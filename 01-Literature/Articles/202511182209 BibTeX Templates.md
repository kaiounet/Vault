---
type: literature
created: 2025-11-18 22:11
source-type: Article
status: active
---

# Literature - 202511182209 BibTeX Templates

## Bibliographic Information
**Author**: RSI 2012 Staff
**Title**: BibTeX Templates
**Year**: 2012
**Publisher/Source**: [MIT](https://web.mit.edu/)
**URL**: https://web.mit.edu/rsi/www/pdfs/bibtex-format.pdf
**Pages/Duration**: 5

## Summary
A comprehensive reference guide for formatting bibliographic entries in BibTeX. Provides templates and examples for 11 different citation types including journal articles, books, theses, technical reports, websites, and various publication statuses. Each template specifies required and optional fields.

## Key Points

- Each BibTeX entry requires a unique key for citation
- Different source types have different required fields
- Author names must be separated by "and"
- Websites require URL formatting and access dates
- Publication status (in press, submitted, unpublished) has specific notation
## Citation Type Templates

### 1. Journal Article

**Required**: author, title, journal, year

```bibtex
@article{key,
  author = {Author A and Author B and Author C},
  title = {Article Title},
  journal = {Journal Name},
  volume = {13},
  year = {2003},
  number = {2},
  pages = {46--129}
}
```

---

### 2. Book

**Required**: author, title, publisher, year

```bibtex
@book{key,
  author = {Author Name},
  title = {Book Title},
  edition = {5},
  publisher = {Publisher Name},
  address = {City State},
  year = {1995}
}
```

---

### 3. Book Series

**Required**: author, title, series, volume, publisher, year

```bibtex
@book{key,
  author = {Author Name},
  title = {Book Title},
  series = {Series Name},
  volume = {3204},
  publisher = {Publisher Name},
  address = {City State},
  year = {1998}
}
```

---

### 4. PhD Thesis

**Required**: author, title, publisher, year

```bibtex
@phdthesis{key,
  author = {Author Name},
  title = {Thesis Title},
  publisher = {University Department},
  address = {City State},
  year = {1996}
}
```

**Note**: For master's thesis, use `@mastersthesis` instead

---

### 5. Technical Report

**Required**: author, title, publisher, year

```bibtex
@techreport{key,
  author = {Author Name},
  title = {Report Title},
  series = {Technical Report},
  volume = {249},
  publisher = {Institution Name},
  address = {City State},
  year = {1985}
}
```

---

### 6. Chapter in Book / Conference Proceedings

**Required**: author, title, booktitle, year

```bibtex
@incollection{key,
  author = {Author Name},
  title = {Chapter Title},
  editor = {Editor Name},
  booktitle = {Book or Conference Title},
  publisher = {Publisher Name},
  address = {City State},
  year = {1987},
  pages = {129--158}
}
```

---

### 7. Website

**Required**: author, title, howpublished (with URL and access date)

```bibtex
@misc{key,
  author = {Author Name},
  title = {Page Title},
  howpublished = {Available at \url{http://www.example.com/page.html} (2005/06/12)}
}
```

**Important**: 
- URL uses `\url{}` command
- Include access date in (YYYY/MM/DD) format
- Escape special characters like underscores with backslash

---

### 8. Article Accepted for Publication (In Press)

**Required**: author, title, journal, note

```bibtex
@unpublished{key,
  author = {Author Name},
  title = {Article Title},
  journal = {Journal Name},
  note = {(in press)}
}
```

---

### 9. Manuscript Submitted for Publication

**Required**: author, title, note, year

```bibtex
@unpublished{key,
  author = {Author Name},
  title = {Manuscript Title},
  note = {Manuscript submitted for publication},
  year = {2012}
}
```

---

### 10. Unpublished Manuscript

**Required**: author, title, note, year

```bibtex
@unpublished{key,
  author = {Author Name},
  title = {Manuscript Title},
  note = {Unpublished Manuscript},
  year = {2012}
}
```

---

### 11. Personal Conversation

**Required**: author, month, year, howpublished

```bibtex
@misc{key,
  author = {Person Name},
  month = {July},
  year = {2012},
  howpublished = {Personal conversation}
}
```

---

## Usage Notes

### Citing in Text
Use `\cite{key}` in your LaTeX document where `key` is the unique identifier you assigned to the bibliography entry.

### Key Selection
Each entry must have a unique key. Common conventions:
- `author2003` - Author last name + year
- `authorYYkeyword` - Author + year + topic keyword
- Whatever system you prefer, stay consistent

### Author Formatting
- Multiple authors separated by `and`
- Format: `FirstName LastName and FirstName LastName`
- Example: `John Smith and Jane Doe and Bob Wilson`

### Special Characters
- Underscores in URLs must be escaped: `\_`
- Use `--` for page ranges (not single hyphen)
- Curly braces protect capitalization: `{NASA}`

---

## Quick Reference Table

| Source Type | Entry Type | Key Required Fields |
|-------------|------------|---------------------|
| Journal Article | `@article` | author, title, journal, year |
| Book | `@book` | author, title, publisher, year |
| Book in Series | `@book` | author, title, series, volume, publisher, year |
| PhD Thesis | `@phdthesis` | author, title, publisher, year |
| Master's Thesis | `@mastersthesis` | author, title, publisher, year |
| Technical Report | `@techreport` | author, title, publisher, year |
| Book Chapter | `@incollection` | author, title, booktitle, year |
| Website | `@misc` | author, title, howpublished |
| In Press | `@unpublished` | author, title, journal, note |
| Submitted | `@unpublished` | author, title, note, year |
| Unpublished | `@unpublished` | author, title, note, year |
| Conversation | `@misc` | author, month, year, howpublished |

---
## My Thoughts
This is a good reminder to when needing a custom bibTeX entry for a specific citation.

## Related Notes
- [[Note title]]
- [[Another related note]]

## Permanent Notes Created
- [[YYYYMMDDHHMM Note title]]
- [[YYYYMMDDHHMM Another note]]

---
Tags: #literature #source/article