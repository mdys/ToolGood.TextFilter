### ��������


``` cs
            MemoryCache.DataFile = "TextFilter-20210923.data";
            MemoryCache.Init();

            var r = TextFilterApplication.FindAll("�����ı�");
            Debug.Assert(r.RiskLevel == IllegalWordsRiskLevel.Pass);

            var t = TextFilterApplication.Replace("�����ı�", '*', false, false);
            Debug.Assert(t.RiskLevel == IllegalWordsRiskLevel.Pass);

```



