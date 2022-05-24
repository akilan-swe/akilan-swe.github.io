# akilan-swe.github.io

**My WebSite**

***

 protected IEnumerable<List<T>> IEnumerableObjectSplitter<T>(IEnumerable<T> data, int requestLimit)
        {
            if (data == null)
            {
                yield return new List<T>();
            }
            else
            {
                int iterationCount = (int)Math.Ceiling((double)data.Count() / requestLimit);
                for (int iteratorIndex = 0; iteratorIndex < iterationCount; iteratorIndex++)
                {
                    yield return data.Skip(iteratorIndex * requestLimit).Take(requestLimit).ToList();
                }
            }
        }
***
