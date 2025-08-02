class Rowts:
    def __init__(self, user_id, emotional_data, creative_data, permissions):
        self.user_id = user_id
        self.emotional_data = emotional_data
        self.creative_data = creative_data
        self.permissions = permissions
        self.registered_creations = []
        self.transaction_log = []

    ## 🌿 Núcleo Criativo
    def registrar_obra(self, obra):
        """
        Salva uma semente criativa na rede Rowts com identidade única.
        """
        if obra not in self.registered_creations:
            self.registered_creations.append(obra)
            print(f"[{self.user_id}] Obra registrada: {obra['titulo']}")
        else:
            print(f"[{self.user_id}] Obra já registrada.")

    def gerar_assinatura_visual(self, obra):
        """
        Cria assinatura 'Sublimação~Martins' espelhada flutuante na imagem.
        """
        return f"Sublimação~Martins :: ⓢ_{obra['titulo']}_[invertido]"

    def ativar_resonancia_criativa(self):
        """
        Estimula visualmente e emocionalmente o criador com base em estado emocional.
        """
        estado = self.emotional_data.get('dominant_emotion', 'neutro')
        tom = {
            'tristeza': 'ouro suave',
            'alegria': 'roxo vibrante',
            'ansiedade': 'azul fluido',
            'neutro': 'luz prateada'
        }.get(estado, 'branco néon')
        print(f"[{self.user_id}] Tom criativo ativado: {tom}")

    ## 💰 Núcleo Comercial
    def ativar_sistema_pagamento(self, valor_usd, metodo):
        """
        Ativa cobrança simbólica ou comercial por envio, entrada ou acesso.
        """
        if not self.permissions.get('pagamento_liberado', False):
            print(f"[{self.user_id}] Permissão de pagamento não concedida.")
            return

        dados = {
            'nome': 'Ramon Martins dos Reis',
            'pix': ramon15martins15@gmail.com
            'email': 'ramon15martins15@gmail.com'
        }

        forma = metodo.lower()
        destino = "Pix" if forma == "pix" else "PayPal/MercadoPago"

        self.transaction_log.append({
            'valor': valor_usd,
            'metodo': destino,
            'para': dados['email' if forma
