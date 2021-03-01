# Nx 関連メモ

- GitHub https://github.com/elixir-nx/nx/tree/main/nx

- Introducing Nx - José Valim https://www.youtube.com/watch?v=fPKMmJpAGWc

```elixir
# tensor

iex> Nx.tensor([1,2,3])[0]
#Nx.Tensor<
  s64
  1
>

iex> t = Nx.tensor([[1, 2], [3, 4]])
#Nx.Tensor<
  s64[2][2]
  [
    [1, 2],
    [3, 4]
  ]
>

iex> t[0]
#Nx.Tensor<
  s64[2]
  [1, 2]
>

iex> t[0][1]
#Nx.Tensor<
  s64
  2
>
```

```elixir
iex> t = Nx.tensor([[1, 2], [3, 4]])
#Nx.Tensor<
  s64[2][2]
  [
    [1, 2],
    [3, 4]
  ]
>

iex> Nx.shape(t)
{2, 2}
iex> t = Nx.tensor([[1, 2], [3, 4]])
#Nx.Tensor<
  s64[2][2]
  [
    [1, 2],
    [3, 4]
  ]
>

iex> Nx.divide(Nx.exp(t), Nx.sum(Nx.exp(t)))
#Nx.Tensor<
  f64[2][2]
  [
    [0.03205860328008499, 0.08714431874203257],
    [0.23688281808991013, 0.6439142598879722]
  ]
>
```
