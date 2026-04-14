# Desafio de Variáveis e Escopos

- **Por que a Secret aparece no log como *** e a variável aparece normalmente?**
O GitHub Actions mascara automaticamente os segredos (Secrets) nos logs para evitar a exposição de dados sensíveis como senhas. Já as variáveis (Vars) são para dados não sensíveis, por isso ficam visíveis.

- **O Job deploy_app consegue ler a variável BUILD_VERSION criada no Job build_app? Por quê?**
Não. Variáveis de Job são isoladas. Como cada Job roda em uma máquina (runner) diferente e independente, um não enxerga as variáveis do outro.
