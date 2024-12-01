### Washington DC Quantum Computing
-----------
This is the presentation + code implementation presented in the [Washington DC Quantum Computing Meetup event](https://www.linkedin.com/events/quantumcomputingforquantumchemi7256029632620019712/comments/) under the title "**Quantum Computing for Quantum Chemistry - Review UCC Methods and Adapt-VQE Algorithms**"

**Getting started**

- Check the file `Abstract.pdf` for the content of the event and also `Presentation.pdf` for the open-source introduction.
- Following steps are to set up the environment for the OpenVQE package and myQLM installation:

#### Step 1: Install `myQLM-fermion`
```bash
git clone https://github.com/myQLM/myqlm-fermion.git
cd myqlm-fermion
pip install -r requirements.txt
pip install .
```
#### Step 2: Set Up a Conda Environment
```bash
conda create --name myenv
conda activate myenv
pip install myqlm==1.9.4
pip install scipy==1.10.1
```

#### Step 3: Install OpenVQE
```bash
git clone https://github.com/OpenVQE/OpenVQE.git
pip install -e .
```
Last step is to clone this git respo as command below 
```bash
git clone https://github.com/huybinhtr/Washington_meet
```

Now you can start to hands-on the the `tutorial.ipynb` that composed of three internal .py file:

- `molecule_ucc_computation.py` initialize the choosen molecules library and to construct UCC ansatz quantum circuit & transform Hamiltonian and cluster operators to qubit representation.
- `HEA_built_model.py` is a library for different extension of Hardware Efficient Ansatz with references.
- `optimization_utils.py` is using the Parameter-Shift Rules (PMRS) for the gradient based optimizer; it stores energies & fidelities also to compute eigenvalues of the Hamiltonian.

**Getting in touch**

For any question about this respo (Package installation, research discussion), don't hesitate to get in touch: huybinhfr4120@gmail.com