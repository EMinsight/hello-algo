<!--
    File: quick_sort.md
    Created Time: 2024-01-05
    Author: krahets (krahets@163.com)
--->

<!-- [file]{quick_sort}-[class]{quick_sort}-[func]{partition} -->
https://pythontutor.com/render.html#code=def%20partition%28nums%3A%20list%5Bint%5D,%20left%3A%20int,%20right%3A%20int%29%20-%3E%20int%3A%0A%20%20%20%20%22%22%22%E5%93%A8%E5%85%B5%E5%88%92%E5%88%86%22%22%22%0A%20%20%20%20%23%20%E4%BB%A5%20nums%5Bleft%5D%20%E4%B8%BA%E5%9F%BA%E5%87%86%E6%95%B0%0A%20%20%20%20i,%20j%20%3D%20left,%20right%0A%20%20%20%20while%20i%20%3C%20j%3A%0A%20%20%20%20%20%20%20%20while%20i%20%3C%20j%20and%20nums%5Bj%5D%20%3E%3D%20nums%5Bleft%5D%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20j%20-%3D%201%20%20%23%20%E4%BB%8E%E5%8F%B3%E5%90%91%E5%B7%A6%E6%89%BE%E9%A6%96%E4%B8%AA%E5%B0%8F%E4%BA%8E%E5%9F%BA%E5%87%86%E6%95%B0%E7%9A%84%E5%85%83%E7%B4%A0%0A%20%20%20%20%20%20%20%20while%20i%20%3C%20j%20and%20nums%5Bi%5D%20%3C%3D%20nums%5Bleft%5D%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20i%20%2B%3D%201%20%20%23%20%E4%BB%8E%E5%B7%A6%E5%90%91%E5%8F%B3%E6%89%BE%E9%A6%96%E4%B8%AA%E5%A4%A7%E4%BA%8E%E5%9F%BA%E5%87%86%E6%95%B0%E7%9A%84%E5%85%83%E7%B4%A0%0A%20%20%20%20%20%20%20%20%23%20%E5%85%83%E7%B4%A0%E4%BA%A4%E6%8D%A2%0A%20%20%20%20%20%20%20%20nums%5Bi%5D,%20nums%5Bj%5D%20%3D%20nums%5Bj%5D,%20nums%5Bi%5D%0A%20%20%20%20%23%20%E5%B0%86%E5%9F%BA%E5%87%86%E6%95%B0%E4%BA%A4%E6%8D%A2%E8%87%B3%E4%B8%A4%E5%AD%90%E6%95%B0%E7%BB%84%E7%9A%84%E5%88%86%E7%95%8C%E7%BA%BF%0A%20%20%20%20nums%5Bi%5D,%20nums%5Bleft%5D%20%3D%20nums%5Bleft%5D,%20nums%5Bi%5D%0A%20%20%20%20return%20i%20%20%23%20%E8%BF%94%E5%9B%9E%E5%9F%BA%E5%87%86%E6%95%B0%E7%9A%84%E7%B4%A2%E5%BC%95%0A%0A%0A%22%22%22Driver%20Code%22%22%22%0Aif%20__name__%20%3D%3D%20%22__main__%22%3A%0A%20%20%20%20nums%20%3D%20%5B2,%204,%201,%200,%203,%205%5D%0A%20%20%20%20partition%28nums,%200,%20len%28nums%29%20-%201%29%0A%20%20%20%20print%28%22%E5%93%A8%E5%85%B5%E5%88%92%E5%88%86%E5%AE%8C%E6%88%90%E5%90%8E%20nums%20%3D%22,%20nums%29&cumulative=false&curInstr=4&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=311&rawInputLstJSON=%5B%5D&textReferences=false

<!-- [file]{quick_sort}-[class]{quick_sort}-[func]{quick_sort} -->
https://pythontutor.com/render.html#code=def%20partition%28nums%3A%20list%5Bint%5D,%20left%3A%20int,%20right%3A%20int%29%20-%3E%20int%3A%0A%20%20%20%20%22%22%22%E5%93%A8%E5%85%B5%E5%88%92%E5%88%86%22%22%22%0A%20%20%20%20%23%20%E4%BB%A5%20nums%5Bleft%5D%20%E4%B8%BA%E5%9F%BA%E5%87%86%E6%95%B0%0A%20%20%20%20i,%20j%20%3D%20left,%20right%0A%20%20%20%20while%20i%20%3C%20j%3A%0A%20%20%20%20%20%20%20%20while%20i%20%3C%20j%20and%20nums%5Bj%5D%20%3E%3D%20nums%5Bleft%5D%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20j%20-%3D%201%20%20%23%20%E4%BB%8E%E5%8F%B3%E5%90%91%E5%B7%A6%E6%89%BE%E9%A6%96%E4%B8%AA%E5%B0%8F%E4%BA%8E%E5%9F%BA%E5%87%86%E6%95%B0%E7%9A%84%E5%85%83%E7%B4%A0%0A%20%20%20%20%20%20%20%20while%20i%20%3C%20j%20and%20nums%5Bi%5D%20%3C%3D%20nums%5Bleft%5D%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20i%20%2B%3D%201%20%20%23%20%E4%BB%8E%E5%B7%A6%E5%90%91%E5%8F%B3%E6%89%BE%E9%A6%96%E4%B8%AA%E5%A4%A7%E4%BA%8E%E5%9F%BA%E5%87%86%E6%95%B0%E7%9A%84%E5%85%83%E7%B4%A0%0A%20%20%20%20%20%20%20%20%23%20%E5%85%83%E7%B4%A0%E4%BA%A4%E6%8D%A2%0A%20%20%20%20%20%20%20%20nums%5Bi%5D,%20nums%5Bj%5D%20%3D%20nums%5Bj%5D,%20nums%5Bi%5D%0A%20%20%20%20%23%20%E5%B0%86%E5%9F%BA%E5%87%86%E6%95%B0%E4%BA%A4%E6%8D%A2%E8%87%B3%E4%B8%A4%E5%AD%90%E6%95%B0%E7%BB%84%E7%9A%84%E5%88%86%E7%95%8C%E7%BA%BF%0A%20%20%20%20nums%5Bi%5D,%20nums%5Bleft%5D%20%3D%20nums%5Bleft%5D,%20nums%5Bi%5D%0A%20%20%20%20return%20i%20%20%23%20%E8%BF%94%E5%9B%9E%E5%9F%BA%E5%87%86%E6%95%B0%E7%9A%84%E7%B4%A2%E5%BC%95%0A%0Adef%20quick_sort%28nums%3A%20list%5Bint%5D,%20left%3A%20int,%20right%3A%20int%29%3A%0A%20%20%20%20%22%22%22%E5%BF%AB%E9%80%9F%E6%8E%92%E5%BA%8F%22%22%22%0A%20%20%20%20%23%20%E5%AD%90%E6%95%B0%E7%BB%84%E9%95%BF%E5%BA%A6%E4%B8%BA%201%20%E6%97%B6%E7%BB%88%E6%AD%A2%E9%80%92%E5%BD%92%0A%20%20%20%20if%20left%20%3E%3D%20right%3A%0A%20%20%20%20%20%20%20%20return%0A%20%20%20%20%23%20%E5%93%A8%E5%85%B5%E5%88%92%E5%88%86%0A%20%20%20%20pivot%20%3D%20partition%28nums,%20left,%20right%29%0A%20%20%20%20%23%20%E9%80%92%E5%BD%92%E5%B7%A6%E5%AD%90%E6%95%B0%E7%BB%84%E3%80%81%E5%8F%B3%E5%AD%90%E6%95%B0%E7%BB%84%0A%20%20%20%20quick_sort%28nums,%20left,%20pivot%20-%201%29%0A%20%20%20%20quick_sort%28nums,%20pivot%20%2B%201,%20right%29%0A%0A%0A%22%22%22Driver%20Code%22%22%22%0Aif%20__name__%20%3D%3D%20%22__main__%22%3A%0A%20%20%20%20%23%20%E5%BF%AB%E9%80%9F%E6%8E%92%E5%BA%8F%0A%20%20%20%20nums%20%3D%20%5B2,%204,%201,%200,%203,%205%5D%0A%20%20%20%20quick_sort%28nums,%200,%20len%28nums%29%20-%201%29%0A%20%20%20%20print%28%22%E5%BF%AB%E9%80%9F%E6%8E%92%E5%BA%8F%E5%AE%8C%E6%88%90%E5%90%8E%20nums%20%3D%22,%20nums%29&cumulative=false&curInstr=5&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=311&rawInputLstJSON=%5B%5D&textReferences=false

<!-- [file]{quick_sort}-[class]{quick_sort_median}-[func]{partition} -->
https://pythontutor.com/render.html#code=def%20median_three%28nums%3A%20list%5Bint%5D,%20left%3A%20int,%20mid%3A%20int,%20right%3A%20int%29%20-%3E%20int%3A%0A%20%20%20%20%22%22%22%E9%80%89%E5%8F%96%E4%B8%89%E4%B8%AA%E5%80%99%E9%80%89%E5%85%83%E7%B4%A0%E7%9A%84%E4%B8%AD%E4%BD%8D%E6%95%B0%22%22%22%0A%20%20%20%20l,%20m,%20r%20%3D%20nums%5Bleft%5D,%20nums%5Bmid%5D,%20nums%5Bright%5D%0A%20%20%20%20if%20%28l%20%3C%3D%20m%20%3C%3D%20r%29%20or%20%28r%20%3C%3D%20m%20%3C%3D%20l%29%3A%0A%20%20%20%20%20%20%20%20return%20mid%20%20%23%20m%20%E5%9C%A8%20l%20%E5%92%8C%20r%20%E4%B9%8B%E9%97%B4%0A%20%20%20%20if%20%28m%20%3C%3D%20l%20%3C%3D%20r%29%20or%20%28r%20%3C%3D%20l%20%3C%3D%20m%29%3A%0A%20%20%20%20%20%20%20%20return%20left%20%20%23%20l%20%E5%9C%A8%20m%20%E5%92%8C%20r%20%E4%B9%8B%E9%97%B4%0A%20%20%20%20return%20right%0A%0Adef%20partition%28nums%3A%20list%5Bint%5D,%20left%3A%20int,%20right%3A%20int%29%20-%3E%20int%3A%0A%20%20%20%20%22%22%22%E5%93%A8%E5%85%B5%E5%88%92%E5%88%86%EF%BC%88%E4%B8%89%E6%95%B0%E5%8F%96%E4%B8%AD%E5%80%BC%EF%BC%89%22%22%22%0A%20%20%20%20%23%20%E4%BB%A5%20nums%5Bleft%5D%20%E4%B8%BA%E5%9F%BA%E5%87%86%E6%95%B0%0A%20%20%20%20med%20%3D%20median_three%28nums,%20left,%20%28left%20%2B%20right%29%20//%202,%20right%29%0A%20%20%20%20%23%20%E5%B0%86%E4%B8%AD%E4%BD%8D%E6%95%B0%E4%BA%A4%E6%8D%A2%E8%87%B3%E6%95%B0%E7%BB%84%E6%9C%80%E5%B7%A6%E7%AB%AF%0A%20%20%20%20nums%5Bleft%5D,%20nums%5Bmed%5D%20%3D%20nums%5Bmed%5D,%20nums%5Bleft%5D%0A%20%20%20%20%23%20%E4%BB%A5%20nums%5Bleft%5D%20%E4%B8%BA%E5%9F%BA%E5%87%86%E6%95%B0%0A%20%20%20%20i,%20j%20%3D%20left,%20right%0A%20%20%20%20while%20i%20%3C%20j%3A%0A%20%20%20%20%20%20%20%20while%20i%20%3C%20j%20and%20nums%5Bj%5D%20%3E%3D%20nums%5Bleft%5D%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20j%20-%3D%201%20%20%23%20%E4%BB%8E%E5%8F%B3%E5%90%91%E5%B7%A6%E6%89%BE%E9%A6%96%E4%B8%AA%E5%B0%8F%E4%BA%8E%E5%9F%BA%E5%87%86%E6%95%B0%E7%9A%84%E5%85%83%E7%B4%A0%0A%20%20%20%20%20%20%20%20while%20i%20%3C%20j%20and%20nums%5Bi%5D%20%3C%3D%20nums%5Bleft%5D%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20i%20%2B%3D%201%20%20%23%20%E4%BB%8E%E5%B7%A6%E5%90%91%E5%8F%B3%E6%89%BE%E9%A6%96%E4%B8%AA%E5%A4%A7%E4%BA%8E%E5%9F%BA%E5%87%86%E6%95%B0%E7%9A%84%E5%85%83%E7%B4%A0%0A%20%20%20%20%20%20%20%20%23%20%E5%85%83%E7%B4%A0%E4%BA%A4%E6%8D%A2%0A%20%20%20%20%20%20%20%20nums%5Bi%5D,%20nums%5Bj%5D%20%3D%20nums%5Bj%5D,%20nums%5Bi%5D%0A%20%20%20%20%23%20%E5%B0%86%E5%9F%BA%E5%87%86%E6%95%B0%E4%BA%A4%E6%8D%A2%E8%87%B3%E4%B8%A4%E5%AD%90%E6%95%B0%E7%BB%84%E7%9A%84%E5%88%86%E7%95%8C%E7%BA%BF%0A%20%20%20%20nums%5Bi%5D,%20nums%5Bleft%5D%20%3D%20nums%5Bleft%5D,%20nums%5Bi%5D%0A%20%20%20%20return%20i%20%20%23%20%E8%BF%94%E5%9B%9E%E5%9F%BA%E5%87%86%E6%95%B0%E7%9A%84%E7%B4%A2%E5%BC%95%0A%0A%0A%22%22%22Driver%20Code%22%22%22%0Aif%20__name__%20%3D%3D%20%22__main__%22%3A%0A%20%20%20%20%23%20%E4%B8%AD%E4%BD%8D%E5%9F%BA%E5%87%86%E6%95%B0%E4%BC%98%E5%8C%96%0A%20%20%20%20nums%20%3D%20%5B2,%204,%201,%200,%203,%205%5D%0A%20%20%20%20partition%28nums,%200,%20len%28nums%29%20-%201%29%0A%20%20%20%20print%28%22%E5%93%A8%E5%85%B5%E5%88%92%E5%88%86%EF%BC%88%E4%B8%AD%E4%BD%8D%E5%9F%BA%E5%87%86%E6%95%B0%E4%BC%98%E5%8C%96%EF%BC%89%E5%AE%8C%E6%88%90%E5%90%8E%20nums%20%3D%22,%20nums%29&cumulative=false&curInstr=5&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=311&rawInputLstJSON=%5B%5D&textReferences=false

<!-- [file]{quick_sort}-[class]{quick_sort_tail_call}-[func]{quick_sort} -->
https://pythontutor.com/render.html#code=def%20partition%28nums%3A%20list%5Bint%5D,%20left%3A%20int,%20right%3A%20int%29%20-%3E%20int%3A%0A%20%20%20%20%22%22%22%E5%93%A8%E5%85%B5%E5%88%92%E5%88%86%22%22%22%0A%20%20%20%20%23%20%E4%BB%A5%20nums%5Bleft%5D%20%E4%B8%BA%E5%9F%BA%E5%87%86%E6%95%B0%0A%20%20%20%20i,%20j%20%3D%20left,%20right%0A%20%20%20%20while%20i%20%3C%20j%3A%0A%20%20%20%20%20%20%20%20while%20i%20%3C%20j%20and%20nums%5Bj%5D%20%3E%3D%20nums%5Bleft%5D%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20j%20-%3D%201%20%20%23%20%E4%BB%8E%E5%8F%B3%E5%90%91%E5%B7%A6%E6%89%BE%E9%A6%96%E4%B8%AA%E5%B0%8F%E4%BA%8E%E5%9F%BA%E5%87%86%E6%95%B0%E7%9A%84%E5%85%83%E7%B4%A0%0A%20%20%20%20%20%20%20%20while%20i%20%3C%20j%20and%20nums%5Bi%5D%20%3C%3D%20nums%5Bleft%5D%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20i%20%2B%3D%201%20%20%23%20%E4%BB%8E%E5%B7%A6%E5%90%91%E5%8F%B3%E6%89%BE%E9%A6%96%E4%B8%AA%E5%A4%A7%E4%BA%8E%E5%9F%BA%E5%87%86%E6%95%B0%E7%9A%84%E5%85%83%E7%B4%A0%0A%20%20%20%20%20%20%20%20%23%20%E5%85%83%E7%B4%A0%E4%BA%A4%E6%8D%A2%0A%20%20%20%20%20%20%20%20nums%5Bi%5D,%20nums%5Bj%5D%20%3D%20nums%5Bj%5D,%20nums%5Bi%5D%0A%20%20%20%20%23%20%E5%B0%86%E5%9F%BA%E5%87%86%E6%95%B0%E4%BA%A4%E6%8D%A2%E8%87%B3%E4%B8%A4%E5%AD%90%E6%95%B0%E7%BB%84%E7%9A%84%E5%88%86%E7%95%8C%E7%BA%BF%0A%20%20%20%20nums%5Bi%5D,%20nums%5Bleft%5D%20%3D%20nums%5Bleft%5D,%20nums%5Bi%5D%0A%20%20%20%20return%20i%20%20%23%20%E8%BF%94%E5%9B%9E%E5%9F%BA%E5%87%86%E6%95%B0%E7%9A%84%E7%B4%A2%E5%BC%95%0A%0Adef%20quick_sort%28nums%3A%20list%5Bint%5D,%20left%3A%20int,%20right%3A%20int%29%3A%0A%20%20%20%20%22%22%22%E5%BF%AB%E9%80%9F%E6%8E%92%E5%BA%8F%EF%BC%88%E5%B0%BE%E9%80%92%E5%BD%92%E4%BC%98%E5%8C%96%EF%BC%89%22%22%22%0A%20%20%20%20%23%20%E5%AD%90%E6%95%B0%E7%BB%84%E9%95%BF%E5%BA%A6%E4%B8%BA%201%20%E6%97%B6%E7%BB%88%E6%AD%A2%0A%20%20%20%20while%20left%20%3C%20right%3A%0A%20%20%20%20%20%20%20%20%23%20%E5%93%A8%E5%85%B5%E5%88%92%E5%88%86%E6%93%8D%E4%BD%9C%0A%20%20%20%20%20%20%20%20pivot%20%3D%20partition%28nums,%20left,%20right%29%0A%20%20%20%20%20%20%20%20%23%20%E5%AF%B9%E4%B8%A4%E4%B8%AA%E5%AD%90%E6%95%B0%E7%BB%84%E4%B8%AD%E8%BE%83%E7%9F%AD%E7%9A%84%E9%82%A3%E4%B8%AA%E6%89%A7%E8%A1%8C%E5%BF%AB%E9%80%9F%E6%8E%92%E5%BA%8F%0A%20%20%20%20%20%20%20%20if%20pivot%20-%20left%20%3C%20right%20-%20pivot%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20quick_sort%28nums,%20left,%20pivot%20-%201%29%20%20%23%20%E9%80%92%E5%BD%92%E6%8E%92%E5%BA%8F%E5%B7%A6%E5%AD%90%E6%95%B0%E7%BB%84%0A%20%20%20%20%20%20%20%20%20%20%20%20left%20%3D%20pivot%20%2B%201%20%20%23%20%E5%89%A9%E4%BD%99%E6%9C%AA%E6%8E%92%E5%BA%8F%E5%8C%BA%E9%97%B4%E4%B8%BA%20%5Bpivot%20%2B%201,%20right%5D%0A%20%20%20%20%20%20%20%20else%3A%0A%20%20%20%20%20%20%20%20%20%20%20%20quick_sort%28nums,%20pivot%20%2B%201,%20right%29%20%20%23%20%E9%80%92%E5%BD%92%E6%8E%92%E5%BA%8F%E5%8F%B3%E5%AD%90%E6%95%B0%E7%BB%84%0A%20%20%20%20%20%20%20%20%20%20%20%20right%20%3D%20pivot%20-%201%20%20%23%20%E5%89%A9%E4%BD%99%E6%9C%AA%E6%8E%92%E5%BA%8F%E5%8C%BA%E9%97%B4%E4%B8%BA%20%5Bleft,%20pivot%20-%201%5D%0A%0A%22%22%22Driver%20Code%22%22%22%0Aif%20__name__%20%3D%3D%20%22__main__%22%3A%0A%20%20%20%20%23%20%E5%BF%AB%E9%80%9F%E6%8E%92%E5%BA%8F%EF%BC%88%E5%B0%BE%E9%80%92%E5%BD%92%E4%BC%98%E5%8C%96%EF%BC%89%0A%20%20%20%20nums%20%3D%20%5B2,%204,%201,%200,%203,%205%5D%0A%20%20%20%20quick_sort%28nums,%200,%20len%28nums%29%20-%201%29%0A%20%20%20%20print%28%22%E5%BF%AB%E9%80%9F%E6%8E%92%E5%BA%8F%EF%BC%88%E5%B0%BE%E9%80%92%E5%BD%92%E4%BC%98%E5%8C%96%EF%BC%89%E5%AE%8C%E6%88%90%E5%90%8E%20nums%20%3D%22,%20nums%29&cumulative=false&curInstr=5&heapPrimitives=nevernest&mode=display&origin=opt-frontend.js&py=311&rawInputLstJSON=%5B%5D&textReferences=false