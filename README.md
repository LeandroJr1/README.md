# README.md
# Fluxograma de Atendimento Comercial para Hotelaria

Este diagrama visualiza as etapas do processo de vendas para conduzir o cliente ao fechamento da reserva, desde a consulta inicial até a confirmação.

## Fluxograma de Atendimento

```mermaid
graph TD
    A[Início: Cliente pergunta sobre diária: Oi gostaria de saber quanto está a diária para X pessoas do dia TAL até dia TAL.] --> B{Resposta do Atendente: Apresentação de Valor Agregado};
    
    B --> C[Eu: Claro! Te passo o valor certinho. Só reforçando: aqui no hotel o valor da diária não é só a hospedagem, mas a sua tranquilidade, já com café da manhã, estacionamento monitorado 24h, Wi-Fi, TV a cabo e chuveiro quente.];
    
    C --> D{Pergunta de Opção: Prefere que eu mostre a opção mais **econômica** ou a mais **confortável**?};
    
    D --> E{Cliente: Mais Econômica};
    E --> F[Apresentar Valor da **Ala Recepção**];
    F --> G{Pergunta de Fechamento: Deseja que eu reserve já para garantir a vaga?};
    G -- Sim --> K;
    G -- Não/Outra Dúvida --> H{Cliente Pede Desconto?};

    D --> I{Cliente: Mais Confortável};
    I --> J[Apresentar Valor da **Ala Nova**];
    J --> K{Pergunta de Fechamento Direto: Posso já deixar a sua reserva garantida?};
    K -- Sim --> M;
    K -- Não --> H;

    H -- Sim --> L[Resposta para Desconto: Reafirmar benefícios e oferecer facilidade. Pergunta: Quer que eu veja a melhor forma de pagamento para você?];
    H -- Não/Diz Vou Pensar --> N{Cliente: Vou Pensar};

    L --> K; 

    N --> O[Resposta para Vou Pensar: Alerta de Escassez. Pergunta: Quer que eu deixe uma **pré-reserva** no seu nome?];
    O -- Sim --> M;
    O -- Não --> P[FIM do Atendimento (Sem Reserva)];

    M[Cliente Aceita Reserva/Pré-reserva] --> Q[Finalização: Perfeito, já vou registrar aqui. Só preciso do seu **nome completo e telefone de contato** para confirmar a reserva.];
    Q --> R[FIM (Reserva Fechada)];
