## Task 1

- Note - completed after Task 2 (required to run training)
- Trained several timess modifying values for 'invalid_pickup_dense_penalty:
    - 0.5 - episode len mean never converges
    - 0.01 - episode len mean converges in 18k steps
    - 0.005 - 13k steps
    - 0.001 - 10k steps

## Task 2
    
- modify __init__ method:
```
            view_height, view_width, _ = agent.observation_space['image'].shape
            # Reassign the "image" observation_space for one-hot encoding observations
            agent.observation_space["image"] = spaces.Box(
                low=0, high=1, shape=(view_height, view_width, dim), dtype=np.uint8
            )
```
    
- modify observation method:
```
    observation["image"] = self.one_hot(observation['image'].astype(int), self.dim_sizes)
```

## Task 3

- This task is accomplished by task 1

## Task 5

- I have no idea what any of this means
