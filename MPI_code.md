#include<stdio.h>
#include<mpi.h>
int main(int argc, char *argv[])
{
	int myrank, processes;
	MPI_Init(&argc, &argv);
	MPI_Comm_rank(MPI_COMM_WORLD, &myrank);
	MPI_Comm_size(MPI_Comm_WORLD, &processes);
	printf("I am process %d of %d\n", myrank, processes);
MPI_Finalize();
return 0;
}
