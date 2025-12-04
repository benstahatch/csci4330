# ============================
# Makefile for Random Forest
# Serial + MPI versions
# ============================

CXX = g++
MPICXX = mpicxx

CXXFLAGS = -O3 -std=c++17
MPIFLAGS = -O3 -std=c++17

SERIAL_SRC = random_forest_serial.cpp
MPI_SRC    = random_forest_mpi.cpp

SERIAL_EXE = rf_serial
MPI_EXE    = rf_mpi

# -------- Targets ----------
all: $(SERIAL_EXE) $(MPI_EXE)

$(SERIAL_EXE): $(SERIAL_SRC)
	$(CXX) $(CXXFLAGS) $< -o $@

$(MPI_EXE): $(MPI_SRC)
	$(MPICXX) $(MPIFLAGS) $< -o $@

clean:
	rm -f $(SERIAL_EXE) $(MPI_EXE)

.PHONY: all clean

