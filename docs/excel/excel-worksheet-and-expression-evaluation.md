---
title: Feuille de calcul Excel et �valuation d�expression
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- expression evaluation [excel 2007],errors in worksheets [Excel 2007],long Unicode strings [Excel 2007],evaluating expressions [Excel 2007],evaluating worksheets [Excel 2007],worksheet evaluation [Excel 2007],worksheet errors [Excel 2007]
localization_priority: Normal
ms.assetid: 47b46a7d-6cfb-4f5b-946d-e0164d18512a
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cf1e0539136435f7d7df6ef348fc92ec4380e132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310982"
---
# <a name="excel-worksheet-and-expression-evaluation"></a>Feuille de calcul Excel et évaluation d’expression

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Le contenu des cellules de feuille de calcul Microsoft Excel est évalué dans l’un des quatre types de données de base :
  
- **Numbers**
    
- **Boolean TRUE** ou **FALSE**
    
- **Strings**
    
- **Errors**
    
Des tableaux de plusieurs types peuvent �galement �tre saisis dans des formules en tant qu�arguments de fonctions ou valeurs �tendant plusieurs cellules dans une formule de tableau.
  
Lorsqu�un utilisateur (ou une macro de commande) saisit un �l�ment dans une cellule, Excel essaie d�interpr�ter l�entr�e et affiche un message d�erreur s�il n�y parvient pas. Si l�entr�e commence par un pr�fixe de cha�ne (un guillemet simple), Excel place tous les caract�res d�entr�e dans la cellule comme pr�vu, sans ajouter de modification. (Le pr�fixe de cha�ne n�est pas affich�.) Si l�entr�e commence par **=**, **+** ou **-**, Excel tente d�interpr�ter l�entr�e comme une formule. Si la syntaxe est incorrecte ou que l��valuation est interrompue, une erreur s�affiche et la cellule est plac�e en mode d��dition. Dans le cas contraire, Excel tente d�identifier, convertir et �valuer les op�rateurs, ainsi que les noms de fonction et leurs arguments. 
  
Les op�randes sont �valu�s de gauche � droite avant l�application de l�op�rateur. Les fonctions sont �valu�es en commen�ant par les op�rateurs ayant la priorit� la plus �lev�e et les plus profonds (les plus imbriqu�s). Si les arguments de fonction ou op�randes ne peuvent pas �tre convertis en types attendus, l��valuation �choue et entra�ne une erreur **#VALUE!**. Lorsqu�un jeton (qui n�est pas une valeur litt�rale) n�est pas reconnu comme une fonction, un nom d�fini ou une �tiquette d�finie, l��valuation �choue et entra�ne une erreur **#NAME?**. 
  
Si l�entr�e ne commence pas par l�un de ces �l�ments, Excel effectue une v�rification par rapport aux mod�les connus d�entr�e, tels que des dates, des heures, des devises, des pourcentages ou des nombres, et r�alise une interpr�tation en cons�quence. Vous pouvez effectuer cette op�ration en suivant des param�tres r�gionaux. Si aucune de ces interpr�tations n�est pertinente, Excel consid�re � nouveau l�entr�e comme une cha�ne et la place dans la cellule sans la modifier.
  
Excel prend en charge d�autres types de donn�es, dont les plus visibles sont les r�f�rences de plage. Excel convertit les r�f�rences vers les valeurs des cellules auxquelles il est fait r�f�rence lors de l��valuation des arguments pour les op�rateurs et fonctions qui ne prennent pas d�arguments de r�f�rence, ou lorsque l�expression dans une formule de cellule est r�duite � une r�f�rence.
  
Excel offre la possibilit� de r�duire une cha�ne de caract�res valide � l�un des quatre types de donn�es de feuille de calcul standard avec la fonction XLM **EVALUATE** et son API C �quivalente **xlfEvaluate**. Entre autres choses, cette fonction permet d��valuer simplement les plages nomm�es dans le code de DLL. Elle diff�re du comportement d�crit pr�c�demment uniquement par le fait qu�au lieu d�afficher des messages d�erreur ou d�activer la modification de cellule, elle renvoie une erreur **#VALUE!** en cas d��chec de l��valuation de l�expression. 
  
## <a name="numbers"></a>Nombres

Tous les nombres de feuille de calcul dans Excel sont repr�sent�s en interne comme une virgule flottante double pr�cision de 8�octets, y compris tous les nombres entiers. Toutefois, l�impl�mentation de ces nombres dans Excel n�est pas enti�rement compatible avec IEEE, comme indiqu� dans le tableau suivant.
  
|**Type**|**Maximum**|**Minimum**|
|:-----|:-----|:-----|
|Double de 8�octets IEEE  <br/> |1.7976931348623157E+308  <br/> |2.2250738585072014E-308  <br/> |
|Feuille de calcul (renvoy�e par la fonction ou coller une valeur)  <br/> |1.7976931348623157E+308  <br/> |2.22507385850721E-308  <br/> |
|Feuille de calcul (saisie manuelle)  <br/> |9.99999999999999E+307  <br/> |2.22507385850721E-308  <br/> |
   
Les nombres IEEE inf�rieurs � la normale (c�est-�-dire, ceux compris dans les plages 2.2250738585072009E�308 � 4.9406564584124654E�324) ne sont pas pris en charge dans les feuilles de calcul Excel, mais sont pris en charge par VBA�Doubles.
  
Si une fonction DLL renvoie IEEE +/- infini ou un double non valide, Excel les convertit en **#NUM!**. Les nombres inf�rieurs � la normale ou inf�rieurs au nombre normal positif minimal dans Excel sont convertis en z�ro positif. La valeur IEEE z�ro n�gatif est prise en charge, autrement dit, elle peut �tre renvoy�e par une fonction DLL et est affich�e en tant que **-0**. (L�op�rateur **\<** ne recherche pas de z�ro n�gatif, donc **=A1\<0** attribue la valeur **TRUE** si A1 contient une valeur z�ro n�gative). 
  
Notez que certains formats de nombre ont des limites plus �troites que celles-ci, par exemple, les dates et les heures. La division enti�re est, en d�finitive, une division de virgule flottante et peut, dans des cas extr�mes, g�n�rer un r�sultat non entier o� le r�sultat pr�cis doit �tre un entier.
  
## <a name="long-unicode-strings"></a>Chaînes Unicode longues

Toutes les chaînes que l�utilisateur voit dans Excel ont depuis de nombreuses versions �t� stock�es en interne en tant que chaînes�Unicode. Les chaînes Unicode de feuille de calcul peuvent comporter jusqu�� 32�767 caract�res (2<sup>15</sup>-1) et peuvent contenir tout caract�re Unicode valide. 
  
Lors de la premi�re introduction de l�API�C, les cha�nes de feuille de calcul �taient des cha�nes d�octets limit�es � une longueur de 255�caract�res, et l�API�C refl�tait ces limitations. Avec Excel 2007, l�API�C est mise � jour pour g�rer les cha�nes Unicode longues Excel. Cela signifie que les fonctions�DLL correctement enregistr�es peuvent accepter des arguments Unicode et renvoyer des cha�nes Unicode.
  
> [!NOTE]
> Les chaînes d�octets sont toujours enti�rement prises en charge dans l�API C pour la compatibilit� descendante. Toutefois, elles ont toujours la m�me limite de 255�caract�res. 
  
## <a name="returning-errors"></a>Renvoi d�erreurs

Excel consid�re comme des erreurs les cellules dans lesquelles il ne peut pas convertir les arguments de fonction ou d�op�rateur en type correct, ou dans lesquelles il ne reconna�t pas une fonction ou un nom d�fini. Ces deux sc�narios ont �t� d�crits pr�c�demment. Lorsque les op�rateurs et fonctions de feuille de calcul int�gr�s �chouent, cela g�n�re aussi des erreurs qui informent l�utilisateur du type d��chec. Vous devez disposer de vos propres fonctions de compl�ment, renvoyant des erreurs coh�rentes avec le comportement dans Excel.
  
### <a name="null"></a>#NULL!

L�erreur **#NULL!** est renvoy�e par certaines fonctions d�informations XLM. Par exemple, l�appel de **GET.DOCUMENT(78)**, ou de la fonction d�API C �quivalente **xlfGetDocument** avec l�argument�78, lorsqu�aucune imprimante n�est install�e, g�n�re le renvoi de cette erreur. Elle peut �galement �tre renvoy�e par certaines fonctions lorsque, par exemple, elles �valuent une cha�ne vide. 
  
Vous pouvez renvoyer cette erreur � partir de votre fonction de compl�ment lorsqu�aucune des autres erreurs ne semble appropri�e.
  
### <a name="div0"></a>#DIV/0!

L�op�rateur de division Excel renvoie l�erreur **#DIV/0!** lorsque le d�nominateur est �gal � z�ro ou � un nombre est trop petit pour �tre repr�sent� comme non nul par Excel. Certaines fonctions qui, par d�finition, impliquent une division peuvent �galement renvoyer cette erreur. Par exemple, **AVERAGE** renvoie cette erreur si aucune des entr�es ne peut �tre convertie en nombre. 
  
Vous devez envisager le renvoi de cette erreur uniquement � partir de votre fonction de compl�ment pour indiquer qu�une division par z�ro a �t� d�tect�e.
  
### <a name="value"></a>#VALUE!

Excel renvoie l�erreur **#VALUE!** si un argument de fonction ou d�op�rateur ne peut pas �tre converti en type requis. Dans le cas des arguments de fonction qui ne peuvent pas �tre convertis, par exemple  `=LN("X")`, Excel n�appelle pas le code de la fonction. Il s�agit d�un point important � retenir lors de l��criture et du d�bogage de vos propres fonctions de compl�ment. 
  
Certaines fonctions renvoient cette erreur si un argument ne peut pas �tre converti dans le code de la fonction. Par exemple,  `DATEVALUE("30-Feb-2007")` �choue avec cette erreur bien que l�argument soit du type appropri�. Dans ce cas, c�est la fonction qui renvoie l�erreur � partir de son code. Certaines fonctions renvoient cette erreur, m�me si les types et les plages de valeur sont autoris�s. Par exemple,  `FIND("a","xyz")` renvoie cette erreur. 
  
Vous devez envisager de renvoyer cette erreur � partir de votre fonction de compl�ment pour indiquer que le type des arguments est incorrect, et que ces derniers n�ont pas pu �tre convertis, ou qu�ils sont en dehors des limites. Toutefois, vous devez envisager de renvoyer **#NUM!** pour les arguments num�riques hors de la plage. Vous devez �galement envisager de renvoyer cette erreur lorsque les arguments de plage ou de tableau ont une forme ou taille incorrecte. 
  
### <a name="ref"></a>#REF!

Excel g�n�re l�erreur **#REF!** au sein d�une expression lorsqu�elle est copi�e vers un emplacement o� la r�f�rence relative obtenue sort des limites. Par exemple, si la cellule�B2 contient la formule  `=A1`, le fait de la copier dans la cellule�B1 entra�ne une formule **=#REF!**. Cette erreur est �galement g�n�r�e dans les formules contenant une r�f�rence qui est remplac�e dans une op�ration de couper-coller ou qui est supprim�e lors de la suppression d�une ligne, d�une colonne ou d�une feuille de calcul. Certaines fonctions pouvant renvoyer des r�f�rences peuvent renvoyer cette erreur, par exemple,  `OFFSET(A1,-1,-1)`. Les noms de feuille de calcul dont les d�finitions contiennent des r�f�rences qui deviennent non valides se voient attribuer cette erreur.
  
Si votre fonction de compl�ment utilise des arguments de r�f�rence, vous devez envisager de renvoyer cette erreur si les r�f�rences ne sont pas valides, ou si vous avez transmis une erreur de r�f�rence. La section sur XLOPER/XLOPER12s dans [Gestion de la m�moire dans Excel](memory-management-in-excel.md) d�crit la fa�on de cr�er des fonctions qui peuvent accepter et renvoyer des arguments de r�f�rence. 
  
### <a name="name"></a>#NAME ?

Excel g�n�re l�erreur **#NAME?** lorsqu�une expression contient un jeton qui n�est pas reconnu comme une fonction ou un nom d�fini. Si votre fonction de compl�ment essaie d�acc�der � un nom d�fini qui n�est pas d�fini, vous devez envisager de renvoyer cette erreur. 
  
### <a name="num"></a>#NUM!

De nombreuses fonctions num�riques et math�matiques int�gr�es dans Excel renvoient l�erreur **#NUM!** lorsqu�une entr�e num�rique est en dehors de la plage autoris�e, par exemple,  `LN(0)`. Vous devez envisager de renvoyer cette erreur � partir de votre fonction de compl�ment pour indiquer qu�une entr�e num�rique est non valide ou hors de la plage.
  
### <a name="na"></a>#N/A

L�erreur **#N/A** est souvent renvoy�e pour indiquer qu�un r�sultat r�ussi ou explicite n�est pas disponible. Par exemple, MATCH avec le troisi�me argument z�ro renvoie cette erreur si une correspondance exacte est introuvable. Cette erreur peut �galement �tre g�n�r�e � l�aide de la fonction **NA**, et si elle est sp�cifiquement d�tect�e par la fonction **ISNA**. Il s�agit donc d�une erreur couramment utilis�e dans les feuilles de calcul pour indiquer une plage de conditions propres � l�application.
  
## <a name="see-also"></a>Voir aussi



[Concepts de programmation Excel](excel-programming-concepts.md)
  
[Programmation avec l�API�C dans Excel](programming-with-the-c-api-in-excel.md)
  
[�valuer les noms et les autres Expressions de formule de feuille de calcul](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[R�f�rence des fonctions XLL SDK API Excel 2013](excel-xll-sdk-api-function-reference.md)

