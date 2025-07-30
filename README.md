# Genetic Algorithm for Video Storage Optimization

A comprehensive implementation of a Genetic Algorithm to solve the video storage optimization problem using multiple crossover and mutation strategies with performance analysis.

## 🎯 Problem Description

Given a collection of 10 videos with different sizes and durations, the goal is to select an optimal subset that:
- Maximizes total viewing time
- Fits within a DVD capacity of 4500 MB
- Uses penalty weights for solutions exceeding capacity

### Dataset
- **Videos**: 10 movies with sizes ranging from 600-1500 MB
- **Durations**: 78-135 minutes
- **DVD Capacity**: 4500 MB
- **Total Content**: 8275 MB, 1117 minutes

## 🧬 Algorithm Features

### Genetic Algorithm Components
- **Population-based search** with tournament selection
- **Fitness function** with penalty weights (Wi = 1.0 for valid solutions, Wi = 0.5 for oversized)
- **Multiple crossover methods**: Single-point and Uniform crossover
- **Multiple mutation methods**: Bit-flip and Interchange mutation
- **Performance tracking** and statistical analysis

### Key Enhancements
- ✅ **Enhanced Crossover Methods**
- ✅ **Enhanced Mutation Strategies** 
- ✅ **Comprehensive Performance Metrics**
- ✅ **Hyperparameter Tuning Analysis**
- ✅ **Statistical Significance Testing**
- ✅ **Visualization and Plotting**

## 📊 Performance Analysis Features

### 1. Basic Experiment
- Single run with performance tracking
- Convergence visualization
- Solution analysis

### 2. Comprehensive Performance Analysis
- Compares all crossover/mutation combinations
- Statistical analysis over multiple runs
- Mean fitness and success rate metrics
- Convergence curve comparisons

### 3. Hyperparameter Tuning
- Grid search over population sizes (20, 50, 100)
- Crossover rates (0.5, 0.7, 0.9)
- Mutation rates (0.01, 0.05, 0.1)


## 📈 Results and Analysis

### Expected Performance Metrics
- **Success Rate**: Percentage of runs achieving fitness ≥ 613
- **Mean Best Fitness**: Average best fitness across multiple runs
- **Convergence Analysis**: Generation-by-generation improvement tracking

### Method Comparison
The code compares four different algorithm variants:
1. Single Point + BitFlip
2. Single Point + Interchange  
3. Uniform + BitFlip
4. Uniform + Interchange

### Visualization
- Convergence curves for different methods
- Performance comparison bar charts
- Statistical analysis plots

## ⚙️ Configuration

### Default Parameters
```python
POPULATION_SIZE = 50
GENERATIONS = 100
CROSSOVER_RATE = 0.7
MUTATION_RATE = 0.1
TOURNAMENT_SIZE = 3
```

### Customization
Modify parameters in the main function calls:
```python
genetic_algorithm_with_performance(
    population_size=100,
    generations=200,
    crossover_rate=0.8,
    mutation_rate=0.05,
    crossover_method='uniform',
    mutation_method='interchange'
)
```

## 📝 Key Functions

### Core Algorithm
- `genetic_algorithm_with_performance()`: Main GA implementation
- `fitness_function()`: Evaluates solution quality with penalties
- `tournament_selection()`: Parent selection mechanism

### Genetic Operators
- `single_point_crossover()` / `uniform_crossover()`: Breeding methods
- `bitflip_mutation()` / `interchange_mutation()`: Variation operators

### Analysis Tools
- `PerformanceMetrics`: Statistical tracking class
- `comprehensive_performance_analysis()`: Multi-method comparison
- `hyperparameter_tuning_analysis()`: Parameter optimization

### Utilities
- `analyze_solution()`: Detailed solution breakdown
- `plot_performance_comparison()`: Visualization functions
- `plot_convergence_comparison()`: Convergence analysis

## 🎯 Sample Output

```
Selected movies: [1, 2, 4, 5, 6, 8]
Total size: 4250 MB (out of 4500 MB)
Total time: 648 minutes (10.8 hours)
Space used: 94.4%
Best fitness: 648.0 minutes
```

## 🔬 Research Applications

This implementation is suitable for:
- **Academic research** in evolutionary computation
- **Optimization problems** with constraint handling
- **Algorithm comparison** studies
- **Parameter sensitivity** analysis
- **Performance benchmarking**

## 📚 Algorithm Theory

### Genetic Algorithm Concepts
- **Selection Pressure**: Tournament selection balances exploration/exploitation
- **Crossover Strategy**: Single-point vs. uniform recombination effects
- **Mutation Impact**: Bit-flip vs. interchange mutation characteristics
- **Penalty Functions**: Handling constraint violations effectively

### Performance Metrics
- **Fitness Landscape**: Understanding problem difficulty
- **Convergence Rate**: Speed of algorithm improvement
- **Success Rate**: Reliability across multiple runs
- **Statistical Significance**: Meaningful performance differences

## 🐛 Troubleshooting

### Common Issues
1. **Import Errors**: Ensure matplotlib and numpy are installed
2. **Memory Issues**: Reduce population size or generations for large problems
3. **Slow Performance**: Use fewer runs in hyperparameter tuning for quick testing

