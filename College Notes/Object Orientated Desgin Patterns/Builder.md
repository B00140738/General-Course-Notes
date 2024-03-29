	TODO: Move each code example up one paragraph.

Builder pattern aims to **separate the construction of a complex object from its representation so that the same construction process can create different representations**. It is used to construct a complex object step by step and the **final step will return the object**. The process of constructing an object should be generic so that it can be used to create different representations of the same object.

1. **Product –** The product class defines the type of the complex object that is to be generated by the builder pattern. 

		interface HousePlan {
			public void setBasement(String basement);

			public void setStructure(String structure);

			public void setRoof(String roof);

			public void setInterior(String interior);
		}

2. **Builder –** This abstract base class defines all of the steps that must be taken in order to correctly create a product. Each step is generally abstract as the actual functionality of the builder is carried out in the concrete subclasses. The getProduct method is used to return the final product. The builder class is often replaced with a simple interface.

		class House implements HousePlan {

			private String basement;
			private String structure;
			private String roof;
			private String interior;

			public void setBasement(String basement){
				this.basement = basement;
			}

			public void setStructure(String structure){
				this.structure = structure;
			}
				etc...
		}

3. **ConcreteBuilder –** There may be any number of concrete builder classes inheriting from Builder. These classes contain the functionality to create a particular complex product.

		interface HouseBuilder {

			public void buildBasement();

			public void buildStructure();

			etc...
			
		}

4. **Director –** The director-class controls the algorithm that generates the final product object. A director object is instantiated and its Construct method is called. The method includes a parameter to capture the specific concrete builder object that is to be used to generate the product. The director then calls methods of the concrete builder in the correct order to generate the product object. On completion of the process, the getProduct method of the builder object can be used to return the product.


### Advantages of Builder Design pattern

1. **The parameters required for the Constructor are reduced**. Along with this, each method call is **easily readable and easy to understand**.

2. Due to the minimal number of parameters needed to be passed to the function, **there is no need to pass in null for optional parameters to the Constructor**.

> [!NOTE]
> An object is just an **instance of a class**.
> 


3. The Object is created/instantiated in a complete state.

4.  
