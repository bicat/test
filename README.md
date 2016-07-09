const int dr[] = {-1, 0, 1, 0};
const int dc[] = {0, 1, 0, -1};

Node walk(const Node& u, int turn) {
  int dir = u.dir;
  if(turn == 1) dir = (dir + 3) % 4; // 逆时针
  if(turn == 2) dir = (dir + 1) % 4; // 顺时针
  return Node(u.r + dr[dir], u.c + dc[dir], dir);
}
1
