---
title: Types de données utilisés par Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- types de données d’enregistrement [excel 2007], Excel des types de données, les chaînes [Excel 2007], [Excel 2007] de numéros, les structures de données [Excel 2007], types de données [Excel 2007]
localization_priority: Normal
ms.assetid: 8740a8fb-ad67-4232-a49b-d78967a786c2
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b32a9beb2f77c12e6b6f2c445672c717a2546386
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782025"
---
# <a name="data-types-used-by-excel"></a>Types de données utilisés par Excel

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel échange plusieurs types ANSI C/C++ et également certaines structures de données spécifiques à Excel. Ceux-ci sont mentionnés ici pour fournir un contexte pour les autres sections, et ils sont abordés en détail dans la rubrique [xlfRegister (formulaire 1)](xlfregister-form-1.md) . 
  
## <a name="ansi-cc-types"></a>Types ANSI C/C++

### <a name="numbers"></a>Nombres

Toutes les versions d’Excel :
  
- double de 8 octets
    
- abréviation [signée] [int] &ndash; utilisé pour les valeurs **booléennes** et les entiers 
    
- court non signé [int]
    
- [signé long] int
    
### <a name="strings"></a>Cha�nes

Toutes les versions d’Excel :
  
- char [signé] \* &ndash; chaînes octet terminée jusqu'à 255 caractères
    
- non signées char \* &ndash; chaînes octets jusqu'à 255 caractères
    
À compter d’Excel 2007 :
  
- non signé court \* &ndash; chaînes Unicode jusqu'à 32 767 caractères, qui peut être terminée ou longueur comptée
    
Tous les numéros de feuille de calcul dans Excel sont stockées sous forme de doubles afin qu’il n’est pas nécessaire (et en fait présente une charge de conversion de petite taille) pour déclarer des fonctions complément échange de types d’entiers avec Excel.
  
Lorsque vous utilisez des types de nombre entier, Excel vérifie que les entrées dans les limites du type, et ils échouent avec **#NUM !** Si en dehors de celles-ci. L’exception est lorsque vous enregistrez une fonction à prendre un argument de **type Boolean** , implémenté à l’aide de short int. Dans ce cas, aucune entrée non nulle est convertie en 1 et valeur zéro est transmise directement. 
  
## <a name="excel-specific-data-structures"></a>Structures de données spécifiques à Excel

Toutes les versions d’Excel :
  
- **FP** &ndash; une structure de tableau à virgule flottante à deux dimensions prenant en charge jusqu'à 65,356 lignes par le nombre maximal de colonnes nombre pris en charge dans la version d’Excel donnée. 
    
- **XLOPER** &ndash; une structure à plusieurs types de données qui peut représenter tous les types de données de feuille de calcul (y compris les erreurs), des entiers, des références de plage, types contrôle flux de feuille de macro XLM et un type de données binaires de stockage interne. 
    
   > [!NOTE]
   > Les chaînes sont représentés sous forme de chaînes d’octets de jusqu'à 255 caractères. 
  
À compter d’Excel 2007 :
  
- **FP12** &ndash; une structure de tableau à virgule flottante à deux dimensions prise en charge de toutes les lignes et les colonnes à compter d’Excel 2007. 
    
- **XLOPER12** &ndash; une structure à plusieurs types de données qui peut représenter tous les types de données de feuille de calcul (y compris les erreurs), des entiers, des références de plage, types contrôle flux de feuille de macro XLM et un type de données binaires de stockage interne. 
    
   > [!NOTE]
   > Les chaînes sont représentées comme des chaînes Unicode longueur comptée jusqu'à 32 767 caractères. 
  
## <a name="registration-data-type-codes"></a>Codes de type de données d’enregistrement

Fonctions XLL sont inscrits en utilisant la fonction API C **xlfRegister**qui prend comme argument troisième une chaîne de caractères qui coder les types de retour et l’argument. Cette chaîne contient également les informations qui indique à Excel si la fonction est volatile, sont thread-safe (commençant dans Excel 2007), sont feuille macro équivalente, et si elle renvoie son résultat en modifiant un argument en place.
  
Le tableau suivant est reproduit et abordé plus en détail dans la rubrique [xlfRegister (formulaire 1)](xlfregister-form-1.md) . Il est reproduite ici afin de fournir un contexte pour le reste de cette section. Par exemple, une fonction qui accepte une chaîne Unicode longueur comptée (commençant dans Excel 2007) peut être décrite comme prenant un C % argument de type. 
  
|Type de données|Passer par valeur|Passer par référence (pointeur)|Commentaires|
|:-----|:-----|:-----|:-----|
|Bool�en  <br/> |A  <br/> |L  <br/> |short (0 = false ou 1 = true)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|Char\*  <br/> ||C, F  <br/> |Chaîne d’octets ASCII terminée  <br/> |
|char non signé\*  <br/> ||D, G  <br/> |Longueur-comptabilisée chaîne d’octets ASCII  <br/> |
|non signé court \* (commençant dans Excel 2007)  <br/> ||C, F %  <br/> |Chaîne de caractères Unicode terminée  <br/> |
|non signé court \* (commençant dans Excel 2007)  <br/> ||% D, G  <br/> |Chaîne à caractères larges longueur comptée Unicode  <br/> |
|court non signé [int]  <br/> |H  <br/> ||WORD  <br/> |
|abréviation [signée] [int]  <br/> |I  <br/> |M  <br/> |16 bits  <br/> |
|[signé long] int  <br/> |J  <br/> |N  <br/> |32 bits  <br/> |
|Tableau  <br/> ||O  <br/> | Passé en tant que trois arguments par référence :  <br/>1. short int \*lignes  <br/>2. short int \*colonnes  <br/>3. double \*tableau  <br/> |
|Tableau  <br/> (commençant dans Excel 2007)  <br/> ||O %  <br/> | Passé en tant que trois arguments par référence :  <br/>1. int \*lignes  <br/>2. int \*colonnes  <br/>3. double \*tableau  <br/> |
|FP  <br/> ||K  <br/> |Structure de tableau à virgule flottante  <br/> |
|FP12  <br/> (commençant dans Excel 2007)  <br/> ||K %  <br/> |Structure de tableau à virgule flottante de grands carreaux  <br/> |
|XLOPER  <br/> ||P  <br/> |Les tableaux et les valeurs de variable de type feuille de calcul  <br/> |
|||R  <br/> |Valeurs, des tableaux et des références de plage  <br/> |
|XLOPER12  <br/> (commençant dans Excel 2007)  <br/> ||Q  <br/> |Les tableaux et les valeurs de variable de type feuille de calcul  <br/> |
|||U  <br/> |Valeurs, des tableaux et des références de plage  <br/> |
   
Les types de **% C**, **F**, **D %**, **% G**, **K %**, **O %**, **Q**et **U** ont été toutes les nouvelles dans Microsoft Office Excel 2007 et ne sont pas pris en charge dans les versions antérieures. Les types de chaînes **F**, **% F**, **G**et **G %** sont utilisés pour les arguments qui sont modifiées en place. Lorsque les arguments **XLOPER** ou **XLOPER12** sont enregistrés en tant que types **P** ou **Q** respectivement, Excel convertit les références de cellule unique à valeurs simples et les références de cellules à des tableaux lorsqu’il prépare les. 
  
Types **P** et **Q** arrivent toujours dans votre fonction comme un des types suivants : **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing**ou **xltypeNil**, mais pas **xltypeRef** ou **xltypeSRef** , car elles sont toujours suppression. 
  
Type **O**, qui est en fait trois arguments sur la pile, a été introduite pour la compatibilité avec les DLL Fortran où les arguments sont passés par référence. Il ne peut pas être utilisé pour retourner une valeur à l’exception de déclaration de l’argument comme valeur de retour de modifier en place et placer les résultats dans les valeurs référencés. Tapez **O %** étend type **O** dans Excel 2007 pour qu’il puisse accéder tableaux qui traitent des sujets supérieures à la grille de Microsoft Office Excel 2003. 
  
## <a name="see-also"></a>Voir aussi

- [xlfRegister (formulaire 1)](xlfregister-form-1.md)
- [Concepts de programmation Excel](excel-programming-concepts.md)
- [R�f�rence des fonctions XLL SDK API Excel 2013](excel-xll-sdk-api-function-reference.md)

