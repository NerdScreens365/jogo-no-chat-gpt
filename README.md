# jogo-no-chat-gpt

#include <stdio.h>
#include <stdbool.h>

#define BOARD_SIZE 8

// Define os caracteres para representar as peças
#define EMPTY ' '
#define WHITE_PIECE 'W'
#define BLACK_PIECE 'B'
#define WHITE_KING 'K'
#define BLACK_KING 'Q'

// Estrutura para representar uma peça no tabuleiro
typedef struct {
    char type;
    bool isKing;
} Piece;

// Função para inicializar o tabuleiro com peças nas posições iniciais
void initializeBoard(Piece board[BOARD_SIZE][BOARD_SIZE]) {
    for (int i = 0; i < BOARD_SIZE; i++) {
        for (int j = 0; j < BOARD_SIZE; j++) {
            if ((i + j) % 2 == 1) {
                if (i < 3) {
                    board[i][j].type = WHITE_PIECE;
                    board[i][j].isKing = false;
                } else if (i > 4) {
                    board[i][j].type = BLACK_PIECE;
                    board[i][j].isKing = false;
                } else {
                    board[i][j].type = EMPTY;
                    board[i][j].isKing = false;
                }
            } else {
                board[i][j].type = EMPTY;
                board[i][j].isKing = false;
            }
        }
    }
}

// Função para imprimir o tabuleiro
void printBoard(Piece board[BOARD_SIZE][BOARD_SIZE]) {
    printf("  a b c d e f g h\n");
    for (int i = 0; i < BOARD_SIZE; i++) {
        printf("%d ", i + 1);
        for (int j = 0; j < BOARD_SIZE; j++) {
            printf("%c ", board[i][j].type);
        }
        printf("%d\n", i + 1);
    }
    printf("  a b c d e f g h\n");
}

int main() {
    Piece board[BOARD_SIZE][BOARD_SIZE];
    initializeBoard(board);

    while (1) {
        // Implemente a lógica do jogo aqui, permitindo que os jogadores façam seus movimentos.

        // Por exemplo, você pode solicitar entradas dos jogadores para mover suas peças.

        printBoard(board);

        // Verifique as condições de vitória ou empate e encerre o jogo quando necessário.

        // Implemente as regras do jogo de damas, como movimento de peças, captura e promoção a rei.

        // Lembre-se de alternar entre os jogadores (branco e preto) após cada movimento.

        // Implemente a lógica para identificar o fim do jogo.

        // Quebra o loop quando o jogo termina
        break;
    }

    // Encerre o jogo e faça qualquer limpeza necessária.

    return 0;
}
