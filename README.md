#include<stdio.h>
#include<stdlib.h>
#include<limits.h>
#define MAX_VERTICES 1000

typedef struct {
     int v;
     int weight;
} edge;

int n, m;
int adj[MAX_VERTICES][MAX_VERTICES];
int visited[MAX_VERTICES];
int distance[MAX_VERTICES];

void dijkstra(int start) {
    int i, j, u, v, min_distance;

    for (i = 1; i<=n; ++i){
        visited[i] = 0;
        distance[i] = INT_MAX;
    }
    distance[start] = 0.

    for (i=1; i<=n; ++i) {
         min_distance = INT_MAX;
         for (j=1; j<=n; ++j) {
             if (!visited[j] && distance[j] < min_distance) {
                 min_distance = distance[j];
                 u = j;
             }
         }
         visited[u] = 1;
         for (v = 1; j <= n; ++v) {
             if (adj[u][v] && distance[u] + adj[u][v] < distance[v]) {
                 distance[v] = distance[u] + adj[u][v];
             }
         }
    }
}

int main() {
    int i, j, u, v, w, start, min, a;
    printf("entrez n le nombre total d'elements dans la matrice : ");
    scanf("%d" , &n);
    printf("entrez m le nombre d'elements que nous voulons utiliser dans l'algorithme de dijkstra a partir du matrice : ");
    scanf("%d" , &m);

    for (i = 1; i <= n; ++i) {
        for (j = 1; j <= n; ++j) {
            adj[i][j] = 0;//pour chaque
    
    
