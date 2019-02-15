[![PyPI version](https://badge.fury.io/py/execution-asserts.svg)](https://badge.fury.io/py/execution-asserts)
[![Downloads](https://pepy.tech/badge/execution-asserts)](https://pepy.tech/project/execution-asserts)
[![Downloads](https://pepy.tech/badge/execution-asserts/month)](https://pepy.tech/project/execution-asserts)


# execution-asserts

A collection of asserts for testing performance of the methods.

## List of asserts
    
   `assertMaximumExecutionTime(max_execution_time_seconds, func, *args, **kwargs)`
   
        
   `assertMaximumMemoryUsage(max_memory_usage, func, *args, **kwargs)`

## How to use 

Look at this sample :
    
    from unittest import TestCase

    from execution_assets import ExecutionTest
    
    def my_method(input_parameter):
        pass
     
     
    class MyTestCase(unittest.TestCase, ExecutionTest):
        def test_execution_time(self):
            self.assertMaximumExecutionTime(0.3, my_method, 'test_value')
            
        def test_memory_usage(self):
            self.assertMaximumMemoryUsage(12, my_method, 'test_value')