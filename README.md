# Mouse2Yoke v2.0 (BETA)

**Voe no X-Plane 12 só com o mouse — no Linux e no Windows. Sem joystick, sem vJoy, sem programa extra.**

Por **Capitão Zelker** · YouTube: [@CaptainZelker](https://www.youtube.com/@CaptainZelker)

> ⚠️ **BETA.** Testado pelo autor no Linux (CachyOS) com o Cessna 172. A versão de Windows está incluída, mas ainda não foi testada — seu feedback é muito bem-vindo (abra uma *Issue* aqui no GitHub).

---

## O que faz

- **Mouse = yoke.** A posição do mouse na tela é a posição do manche (borda da tela = deflexão total).
- Aparece só uma pequena **cruz +** na tela. A caixinha padrão de mouse do X-Plane é escondida automaticamente.
- **Segurar o botão esquerdo = rudder.** Mexa o mouse para os lados (as duas barras verdes mostram o curso). Ao soltar, o rudder volta ao neutro.
- **Curva coordenada:** no ar, o rudder acompanha o roll de leve e a bolinha fica no centro (sem precisar de pedais).
- **Taxiar com o mouse:** no solo, mexer o mouse para os lados esterça a roda do nariz. O efeito some entre 15 e 40 kt para não atrapalhar a corrida de decolagem.
- **Liga/desliga com uma tecla.** Ao desligar, o manche **fica exatamente onde estava**, como se você o segurasse com a mão (a curva continua). Ao ligar de novo não há tranco: uma cruz **amarela** mostra onde o manche está, e o mouse assume quando você passa por ela.
- O botão direito continua olhando em volta normalmente.

## Requisitos

X-Plane 12 · Windows 64 bits ou Linux 64 bits (qualquer distribuição recente). macOS ainda não está incluído.

## Instalação

1. Baixe o **`Mouse2Yoke_v2.0_BETA.zip`** na página de [Releases](../../releases).
2. Extraia o zip e copie a pasta **`Mouse2Yoke`** para dentro de `X-Plane 12/Resources/plugins/`.
   Deve ficar assim:
   - Linux: `Resources/plugins/Mouse2Yoke/lin_x64/Mouse2Yoke.xpl`
   - Windows: `Resources/plugins/Mouse2Yoke/win_x64/Mouse2Yoke.xpl`
3. Abra o X-Plane 12. Vá em **Settings → Keyboard**, procure **"Mouse2Yoke: toggle mouse yoke control"** e atribua uma tecla (por exemplo, **Y**).
4. Carregue um avião, aperte a tecla e voe com o mouse.

## Menu

**Plugins → Mouse2Yoke** liga/desliga: mouse yoke, coordenação automática de rudder, direção da roda do nariz no solo, soltar e centrar o manche, e recarregar o `settings.ini`.

## Ajustes

Tudo pode ser ajustado no arquivo `Mouse2Yoke/settings.ini` (todos os itens estão comentados). Depois de editar, use *Plugins → Mouse2Yoke → Reload settings.ini*. Os mais úteis:

| Opção | Para que serve |
|---|---|
| `coord_gain` | Quanto de rudder nas curvas (aumente se a bolinha escapar para fora) |
| `taxi_gain` | Força da direção no solo |
| `rudder_distance` | Quanto o mouse precisa andar para rudder total |
| `deadzone` / `expo` | Zona morta e suavização no centro |
| `invert_pitch` | Inverte o pitch |
| `crosshair_size` | Tamanho da cruz |

## Observações

- Com o mouse yoke **ligado**, o botão **esquerdo** pertence ao plugin (rudder). Para clicar no cockpit, desligue com a tecla — o manche continua onde estava.
- Se algo não funcionar, mande o `Log.txt` da pasta do X-Plane (procure as linhas que começam com `[Mouse2Yoke]`).

---

📺 Um guia completo em vídeo vem no canal: [youtube.com/@CaptainZelker](https://www.youtube.com/@CaptainZelker)

*A ideia foi inspirada no BetterMouseYoke, de Torben Könke (X-Plane 11). O Mouse2Yoke é um plugin novo e independente, escrito do zero para o X-Plane 12, sem ligação com o original. Sem ligação com a Laminar Research.*
