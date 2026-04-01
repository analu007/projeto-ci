Validação Parte 3:
analu007@adrianinha:~/meu-projeto-ci$ act -l
INFO[0000] Using docker host 'unix:///var/run/docker.sock', and daemon socket 'unix:///var/run/docker.sock'
Stage  Job ID             Job name           Workflow name     Workflow file              Events
0      teste-basico       teste-basico       Hello World       01-hello-local.yml         workflow_dispatch
0      setup-e-lint       setup-e-lint       Pipeline oficial  02-pipeline-principal.yml  push
1      scan-de-seguranca  scan-de-seguranca  Pipeline oficial  02-pipeline-principal.yml  push
1      testes-unitarios   testes-unitarios   Pipeline oficial  02-pipeline-principal.yml  push
2      build-e-deploy     build-e-deploy     Pipeline oficial  02-pipeline-principal.yml  push



analu007@adrianinha:~/meu-projeto-ci$ act -n
INFO[0000] Using docker host 'unix:///var/run/docker.sock', and daemon socket 'unix:///var/run/docker.sock'
*DRYRUN* [Pipeline oficial/setup-e-lint] ⭐ Run Set up job
*DRYRUN* [Pipeline oficial/setup-e-lint] 🚀  Start image=catthehacker/ubuntu:act-latest
*DRYRUN* [Pipeline oficial/setup-e-lint]   🐳  docker pull image=catthehacker/ubuntu:act-latest platform= username= forcePull=true
*DRYRUN* [Pipeline oficial/setup-e-lint]   🐳  docker create image=catthehacker/ubuntu:act-latest platform= entrypoint=["tail" "-f" "/dev/null"] cmd=[] network="host"
*DRYRUN* [Pipeline oficial/setup-e-lint]   🐳  docker run image=catthehacker/ubuntu:act-latest platform= entrypoint=["tail" "-f" "/dev/null"] cmd=[] network="host"
*DRYRUN* [Pipeline oficial/setup-e-lint]   ✅  Success - Set up job
*DRYRUN* [Pipeline oficial/setup-e-lint] ⭐ Run Main echo "Analisando qualidade do código..."
*DRYRUN* [Pipeline oficial/setup-e-lint]   ✅  Success - Main echo "Analisando qualidade do código..." [127.268099ms]
*DRYRUN* [Pipeline oficial/setup-e-lint] ⭐ Run Complete job
*DRYRUN* [Pipeline oficial/setup-e-lint] Cleaning up container for job setup-e-lint
*DRYRUN* [Pipeline oficial/setup-e-lint]   ✅  Success - Complete job
*DRYRUN* [Pipeline oficial/setup-e-lint] 🏁  Job succeeded
*DRYRUN* [Pipeline oficial/testes-unitarios ] ⭐ Run Set up job
*DRYRUN* [Pipeline oficial/testes-unitarios ] 🚀  Start image=catthehacker/ubuntu:act-latest
*DRYRUN* [Pipeline oficial/scan-de-seguranca] ⭐ Run Set up job
*DRYRUN* [Pipeline oficial/scan-de-seguranca] 🚀  Start image=catthehacker/ubuntu:act-latest
*DRYRUN* [Pipeline oficial/testes-unitarios ]   🐳  docker pull image=catthehacker/ubuntu:act-latest platform= username= forcePull=true
*DRYRUN* [Pipeline oficial/scan-de-seguranca]   🐳  docker pull image=catthehacker/ubuntu:act-latest platform= username= forcePull=true
*DRYRUN* [Pipeline oficial/testes-unitarios ]   🐳  docker create image=catthehacker/ubuntu:act-latest platform= entrypoint=["tail" "-f" "/dev/null"] cmd=[] network="host"
*DRYRUN* [Pipeline oficial/testes-unitarios ]   🐳  docker run image=catthehacker/ubuntu:act-latest platform= entrypoint=["tail" "-f" "/dev/null"] cmd=[] network="host"
*DRYRUN* [Pipeline oficial/testes-unitarios ]   ✅  Success - Set up job
*DRYRUN* [Pipeline oficial/scan-de-seguranca]   🐳  docker create image=catthehacker/ubuntu:act-latest platform= entrypoint=["tail" "-f" "/dev/null"] cmd=[] network="host"
*DRYRUN* [Pipeline oficial/scan-de-seguranca]   🐳  docker run image=catthehacker/ubuntu:act-latest platform= entrypoint=["tail" "-f" "/dev/null"] cmd=[] network="host"
*DRYRUN* [Pipeline oficial/scan-de-seguranca]   ✅  Success - Set up job
*DRYRUN* [Pipeline oficial/scan-de-seguranca] ⭐ Run Main echo "Procurando vulnerabilidades..."
*DRYRUN* [Pipeline oficial/testes-unitarios ] ⭐ Run Main echo "Rodando testes unitários..."
*DRYRUN* [Pipeline oficial/testes-unitarios ]   ✅  Success - Main echo "Rodando testes unitários..." [103.115315ms]
*DRYRUN* [Pipeline oficial/testes-unitarios ] ⭐ Run Complete job
*DRYRUN* [Pipeline oficial/testes-unitarios ] Cleaning up container for job testes-unitarios
*DRYRUN* [Pipeline oficial/scan-de-seguranca]   ✅  Success - Main echo "Procurando vulnerabilidades..." [103.369751ms]
*DRYRUN* [Pipeline oficial/scan-de-seguranca] ⭐ Run Complete job
*DRYRUN* [Pipeline oficial/scan-de-seguranca] Cleaning up container for job scan-de-seguranca
*DRYRUN* [Pipeline oficial/scan-de-seguranca]   ✅  Success - Complete job
*DRYRUN* [Pipeline oficial/scan-de-seguranca] 🏁  Job succeeded
*DRYRUN* [Pipeline oficial/testes-unitarios ]   ✅  Success - Complete job
*DRYRUN* [Pipeline oficial/testes-unitarios ] 🏁  Job succeeded
*DRYRUN* [Pipeline oficial/build-e-deploy   ] ⭐ Run Set up job
*DRYRUN* [Pipeline oficial/build-e-deploy   ] 🚀  Start image=catthehacker/ubuntu:act-latest
*DRYRUN* [Pipeline oficial/build-e-deploy   ]   🐳  docker pull image=catthehacker/ubuntu:act-latest platform= username= forcePull=true
*DRYRUN* [Pipeline oficial/build-e-deploy   ]   🐳  docker create image=catthehacker/ubuntu:act-latest platform= entrypoint=["tail" "-f" "/dev/null"] cmd=[] network="host"
*DRYRUN* [Pipeline oficial/build-e-deploy   ]   🐳  docker run image=catthehacker/ubuntu:act-latest platform= entrypoint=["tail" "-f" "/dev/null"] cmd=[] network="host"
*DRYRUN* [Pipeline oficial/build-e-deploy   ]   ✅  Success - Set up job
*DRYRUN* [Pipeline oficial/build-e-deploy   ] ⭐ Run Main echo "Gerando artefato e fazendo deploy..."
*DRYRUN* [Pipeline oficial/build-e-deploy   ]   ✅  Success - Main echo "Gerando artefato e fazendo deploy..." [99.094147ms]
*DRYRUN* [Pipeline oficial/build-e-deploy   ] ⭐ Run Complete job
*DRYRUN* [Pipeline oficial/build-e-deploy   ] Cleaning up container for job build-e-deploy
*DRYRUN* [Pipeline oficial/build-e-deploy   ]   ✅  Success - Complete job
*DRYRUN* [Pipeline oficial/build-e-deploy   ] 🏁  Job succeeded


Validação Parte 4:
A partir do Stage em que eles estão, no caso desse workflow ambos estão no stage 1.
