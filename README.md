# hello-word

//邻接表存储的图实现DFS 
 void Visit(Vertex V){
 	cout<<"正在访问顶点"<<V<<endl; 
 }
 
 //Visit[]为全局变量，已经初始化为false
 void DFS(LGraph Graph, Vertex V, void (*Visit)(Vertex))
 {//以V为出发点对邻接表存储的图Graph进行DFS搜索 
 	ptrToAdjVNode W;
	 Visit(V);      //访问第V个节点 
	 Visited[V]=true;
	 
	 for(W=Graph->G[V].FirstEdge;W;W=W->Next)//对V的每个邻接节点w->Adjv 
	 if(!Visited[W->AdjV])//若w->adjv未被放问 
	 	DFS(Graph,W->Adjv,visit); //则递归访问之 
  } 
