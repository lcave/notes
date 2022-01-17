# Deep Models

Often when learning object oritented design, we reach for nouns and verbs in our requirement documentation to create our initial models and methods. For example, requirements for a Shipping Company:

- **Ships** hold many **Containers** 
- **Ships** **load** and **unload** **Containers**

Looking at these requierments we would likely end up with:

```ruby
class Ship 
	has_many: Containers

	def load(container)
		# load container onto ship
	end

	def unload(container)
		# unload container onto dock
	end
end

class Container
	belongs_to Ship
	has_many Contents
end
```

However, this is not a particularly useful model for a real-world shipping business. In reality the domain, according to domain experts, looks more like: 

```ruby
class Voyage
	has_one Vessel

	def accept_lading(bill_of_lading_details)
		# receive cargo for transport
	end

	def transfer_lading
		# transfer legal responsibility of cargo to next vessel 
	end
end

class Vessel
	belongs_to Voyage
end

```

This model is only incidentally concerned with Ships, which are merely a method of completing a voyage, and Containers, which are an unimportant operational detail. The Ship is secondary, and can be substituted at the last minute for maintenance or a slipping schedule, while the Voyage goes on as planned. Similarly, The physical movement of the cargo took a back seat to the transfers of legal responsibility for that cargo.

##### Almost all Deep Models share a simple, though possibly abstract, language used by experts in the business it represents. 

