flowchart TD
    A[Início] --> B[Usuário acessa o site.]
    B --> C{Já possui cadastro?}
    C -->|Sim| D[Fazer login.]
    C -->|Não| E[Criar uma conta.]
    D --> F[Usuário navega e visualiza produtos disponíveis em estoque.]
    E --> F
    F --> G{Adicionar itens ao carrinho ou lista de desejos?}
    G -->|Carrinho| H[Usuário revisa pedido no carrinho.]
    G -->|Lista de Desejos| I{Deseja continuar comprando?}
    I -->|Sim| F
    I -->|Não| Z[FIM]
    H --> J{Gostaria de finalizar sua compra e prosseguir para o pagamento?}
    J -->|Sim| K[Sistema verifica novamente o estoque.]
    J -->|Não| Z
    K --> L[Cliente faz Checkout.]
    L --> M[Gateway de pagamento.]
    M --> N{Pagamento aprovado?}
    N -->|Sim| O[Pedido confirmado no sistema e e-mail é enviado.]
    N -->|Não| P{Solicitar novo método de pagamento ou deseja encerrar?}
    P -->|Novo método| L
    P -->|Encerrar| Z
    O --> Q[Pedido enviado para expedição.]
    Q --> R[Pedido despachado.]
    R --> S[Usuário recebe status e código de rastreio.]
    S --> T[Pedido entregue!]
    T --> Z[FIM]
