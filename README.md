# What is directory in ipfs?


Let's add a directory `1` with subdirectories and files to ipfs:

`
➜  ipfs add -r ./1
added QmUNLLsPACCz1vLxQVkXqqLX5R1X345qqfHbsf67hvA3Nn 1/app/images
added QmeiFqNGeiAdAUjZrZUb92mVAGKuWDyfqt1isMn8wqDbiL 1/app/index.html
added QmVPYc58NruJoTQ7juSXBQauSceDmbDR2b8qGRkU6qQBAt 1/app/javascripts/app.js
added QmeJieQhM5t3BV4uyqazY33u69cw8YtaFNk84P2NK3uzMv 1/app/javascripts
added QmP8d2MdAVfHgmkEcprHgMZTucr4FSpPR82fuCj7i1z2D9 1/app/stylesheets/app.css
added QmUSUXca2hrwLTfTr9rxwQ1yXqSAAyPF7UY6dNXUknBqJU 1/app/stylesheets
added QmPYitXxxr1N7B8tEfAG9xpruzzJonwuG1aFMLvGaFxLLy 1/app
added QmYk4LCpPJu6sQkNDeXwtFy3dMNnoP5dEpo71kJKAACzUd 1/contracts/MetaCoin.sol
added QmbLzy6SjZsSPdtsm8p2x8arbJnbyeYzmrUrvUYnpba6MV 1/contracts
added QmfSnGmfexFsLDkbgN76Qhx2W8sxrNDobFEQZ6ER5qg2wW 1/environments/development/config.json
added QmNf6yXTR3ned6F5C5XNQvFpNLAR5nnmodoY5rdX4eqdDy 1/environments/development/contracts/MetaCoin.sol.js
added QmRuFNzZ8exicCQYikx3LTLNaMX95ov8nyKJesJ5Kc7f9w 1/environments/development/contracts
added QmZnpR9u9s8XV6rFnHPtooHDgazKuMkZPWR43EwBYKBj97 1/environments/development
added QmfSnGmfexFsLDkbgN76Qhx2W8sxrNDobFEQZ6ER5qg2wW 1/environments/production/config.json
added QmesFjLtRm8GvaUJFLPSijUKcKS545UbiVwdGEx5GTyBDU 1/environments/production
added QmfSnGmfexFsLDkbgN76Qhx2W8sxrNDobFEQZ6ER5qg2wW 1/environments/staging/config.json
added QmesFjLtRm8GvaUJFLPSijUKcKS545UbiVwdGEx5GTyBDU 1/environments/staging
added QmfSnGmfexFsLDkbgN76Qhx2W8sxrNDobFEQZ6ER5qg2wW 1/environments/test/config.json
added QmesFjLtRm8GvaUJFLPSijUKcKS545UbiVwdGEx5GTyBDU 1/environments/test
added Qmaaaq6JZ26ap72DfHwGmAhqpYm93iUwy16qtXBrxB7FxR 1/environments
added QmbMLd77pEiJz7b66YzybDhWpdqg5WpgJWjBRBBVEUuq8k 1/test/metacoin.js
added QmYJKwAWhg9DYR2WDSovWjcrxrVdTiVrKj5MiGsjgTvdRm 1/test
added Qmac8c1rhiaNHfuPWrvdhzXVZ6qs2SSirXVgaLqC4yjn9D 1/truffle.json
added QmfDdArE3J38KA6YL3mygnksKiX5AB9CoT5yFNY8ECMvSu 1
`

Let's make a tree out of it:

````
➜  tree 1
1
├── app
│   ├── images
│   ├── index.html
│   ├── javascripts
│   │   └── app.js
│   └── stylesheets
│       └── app.css
├── contracts
│   └── MetaCoin.sol
├── environments
│   ├── development
│   │   ├── config.json
│   │   └── contracts
│   │       └── MetaCoin.sol.js
│   ├── production
│   │   └── config.json
│   ├── staging
│   │   └── config.json
│   └── test
│       └── config.json
├── test
│   └── metacoin.js
└── truffle.json

12 directories, 11 files
```

Combine both hashes and tree:

`graphmd QmfDdArE3J38KA6YL3mygnksKiX5AB9CoT5yFNY8ECMvSu | dot -Tpng >graph.png`

![Tree](https://github.com/igorbarinov/ipfs-playground/blob/master/img/graph.png "Tree")
