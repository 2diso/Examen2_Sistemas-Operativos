# Examen2_Sistemas-Operativos

# Actividad 4 - Troubleshooting
# Snippet 1 corregido:
on:
  push:
    branches: [main]
  pull_request:
    branches: [main, develop]

# Snippet 2 corregido:
env:
  VERCEL_TOKEN: ${{ secrets.VERCEL_TOKEN }}

# Snippet 3 corregido:
strategy:
  matrix:
    node-version: [16, 18]