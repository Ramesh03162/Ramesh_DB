name: Terraform

on:
  push:
    branches:
      - master

jobs:
  terraform:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v2

      - name: Setup Terraform
        uses: hashicorp/setup-terraform@v1

      - name: Terraform Init
        run: terraform init

      - name: Terraform Plan
        run: terraform plan

      - name: Terraform Apply
        run: terraform apply -auto-approve
        env:
             SNOWFLAKE_ACCOUNT: ${{ secrets.https://ichuvnn-vy07960.snowflakecomputing.com}}
             SNOWFLAKE_USERNAME: ${{ secrets.Ramesh031 }}
             SNOWFLAKE_PASSWORD: ${{ secrets.Ram@159h5a0317 }}
