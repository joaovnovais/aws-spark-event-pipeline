# Pipeline de Processamento de Eventos com Spark e S3 (AWS)

## Descrição
Este projeto implementa um pipeline de ingestão e processamento de dados de eventos em formato JSON, armazenados no Amazon S3. O processamento é realizado com PySpark e os resultados são gravados de volta no S3 em formato Parquet.

## Estrutura do Projeto

projeto7-pipeline-eventos/
├── scripts/
│ └── processar_eventos.py
├── requirements.txt
└── README.md


## Tecnologias Utilizadas
- AWS S3
- Apache Spark (PySpark)
- Python 3.10+
- VS Code (opcional)

## Pipeline de Dados
1. Dados brutos JSON são lidos do S3 (`/eventos/raw/`)
2. Apenas eventos com ação `compra` são filtrados
3. Resultado é salvo em S3 como `.parquet` em `/eventos/processed/`

## Como Executar
1. Configure o ambiente virtual e instale as dependências:
```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

