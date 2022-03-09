---
title: Types de données utilisés par Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- types de données d’inscription [Excel 2007], types de données Excel [Excel 2007], chaînes [Excel 2007], nombres [Excel 2007], structures de données [Excel 2007], types de données [Excel 2007]
ms.assetid: 8740a8fb-ad67-4232-a49b-d78967a786c2
ms.localizationpriority: high
ms.openlocfilehash: 2a252cfce0e872905d6820dd11738cd98ce49ff0
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372037"
---
# <a name="data-types-used-by-excel"></a>Types de données utilisés par Excel

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
Microsoft Excel échange plusieurs types ANSI C/C++ et également certaines structures de données propres à Excel. Ceux-ci sont mentionnés ici pour fournir un contexte pour d’autres sections, et sont décrits en détail dans la rubrique [xlfRegister (formulaire 1)](xlfregister-form-1.md).
  
## <a name="ansi-cc-types"></a>Types ANSI C/C++

### <a name="numbers"></a>Nombres

Toutes les versions d’Excel :
  
- Double de 8 octets

- [signed] short [int] &ndash; utilisé pour les valeurs **booléennes** et les entiers

- unsigned short [int]

- [signed long] int

### <a name="strings"></a>Chaînes

Toutes les versions d’Excel :
  
- [signed] char \* &ndash; chaînes d’octets se terminant par null et comptant 255 caractères maximum

- unsigned char \* &ndash; chaînes d’octets de longueur comptée de 255 caractères maximum

Introduit dans Excel 2007 :
  
- unsigned short \* &ndash; chaînes Unicode composées de 32 767 caractères maximum, de longueur comptée ou pouvant se terminer par null

Tous les nombres de feuille de calcul dans Excel sont stockés comme doubles de sorte qu’il n’est pas nécessaire (et en réalité cela introduit une petite conversion) de déclarer de fonctions de complément lors de l’échange de types entier avec Excel.
  
Là où vous utilisez des types entier, Excel vérifie que les entrées sont dans les limites du type et une erreur **#NUM!** se produit si elles se trouvent en dehors. L’exception se produit lorsque vous inscrivez une fonction pour prendre un argument **booléen** implémenté à l’aide de short int. Dans ce cas, toute entrée non zéro est convertie en 1, et zéro est passé directement.
  
## <a name="excel-specific-data-structures"></a>Structures de données propres à Excel

Toutes les versions d’Excel :
  
- **FP** &ndash; structure de tableau à virgule flottante à deux dimensions prenant en charge jusqu'à 65 356 lignes par le nombre maximal de colonnes pris en charge dans la version donnée d’Excel.

- **XLOPER** &ndash; structure de données de type multiple qui peut représenter tous les types de données de feuille de calcul (y compris les erreurs), entiers, références de plage, types de contrôles de flux de feuille macro XLM et un type de données de stockage binaire interne.

   > [!NOTE]
   > Les chaînes sont représentées sous forme de chaînes de longueur comptée de 255 caractères maximum.
  
Introduit dans Excel 2007 :
  
- **FP12** &ndash; structure de tableau à virgule flottante à deux dimensions prenant en charge toutes les lignes et les colonnes (intoduit dans Excel 2007).

- **XLOPER12** &ndash; structure de données de type multiple qui peut représenter tous les types de données de feuille de calcul (y compris les erreurs), entiers, références de plage, types de contrôles de flux de feuille macro XLM et un type de données de stockage binaire interne.

   > [!NOTE]
   > Les chaînes sont représentées sous forme de chaînes Unicode de longueur comptée de 32 767 caractères maximum.
  
## <a name="registration-data-type-codes"></a>Codes de type de données d’inscription

Les fonctions XLL sont inscrites à l’aide de la fonction API C **xlfRegister**, qui prend comme troisième argument une chaîne de lettres qui encode les types de retour et d’argument. Cette chaîne contient également des informations qui indiquent à Excel si la fonction est volatile, thread-safe (introduit dans Excel 2007), est équivalente à une feuille macro et si elle renvoie son résultat en modifiant un argument en place.
  
Le tableau suivant est reproduit et décrit plus en détail dans la rubrique [xlfRegister (formulaire 1)](xlfregister-form-1.md). Il est reproduit ici afin de fournir un contexte pour le reste de cette section. Par exemple, une fonction qui prend une chaîne Unicode longueur comptée (introduit dans Excel 2007) peut être décrite comme prenant un argument de type C%.
  
|Type de données|Passer par valeur|Passer par référence (pointeur)|Commentaires|
|:-----|:-----|:-----|:-----|
|Booléen  <br/> |A  <br/> |L  <br/> |short (0 = False ou 1 = True)  <br/> |
|double  <br/> |B  <br/> |E  <br/> ||
|char \*  <br/> ||C, F  <br/> |Chaîne d’octets ASCII se terminant par null  <br/> |
|unsigned char \*  <br/> ||D, G  <br/> |Chaîne d’octets ASCII de longueur comptée  <br/> |
|unsigned short \* (introduit dans Excel 2007)  <br/> ||C%, F%  <br/> |Chaîne de caractères larges Unicode se terminant par null  <br/> |
|unsigned short \* (introduit dans Excel 2007)  <br/> ||D%, G%  <br/> |Chaîne de caractères larges Unicode de longueur comptée  <br/> |
|unsigned short [int]  <br/> |H  <br/> ||WORD  <br/> |
|[signed] short [int]  <br/> |I  <br/> |M  <br/> |16 bits  <br/> |
|[signed long] int  <br/> |J  <br/> |N  <br/> |32 bits  <br/> |
|Tableau  <br/> ||O  <br/> | Passé comme trois arguments par référence :  <br/>1. short int \*lignes  <br/>2. short int \*colonnes  <br/>3. double \*tableau  <br/> |
|Tableau  <br/> (introduit dans Excel 2007)  <br/> ||O%  <br/> | Passé comme trois arguments par référence :  <br/>1. int \*lignes  <br/>2. int \*colonnes  <br/>3. double \*tableau  <br/> |
|FP  <br/> ||K  <br/> |Structure de tableau à virgule flottante  <br/> |
|FP12  <br/> (introduit dans Excel 2007)  <br/> ||K%  <br/> |Structure de tableau à virgule flottante à grande grille  <br/> |
|XLOPER  <br/> ||P  <br/> |Tableaux et valeurs de feuille de calcul de type variable  <br/> |
|||R  <br/> |Valeurs, tableaux et références de plage  <br/> |
|XLOPER12  <br/> (introduit dans Excel 2007)  <br/> ||Q  <br/> |Tableaux et valeurs de feuille de calcul de type variable  <br/> |
|||U  <br/> |Valeurs, tableaux et références de plage  <br/> |

Les types **C%**, **F%**, **D%**, **G%**, **K%**, **O%**, **Q** et **U** étaient tous nouveaux dans Microsoft Office Excel 2007 et ne sont pas pris en charge dans les versions antérieures. Les types de chaînes **F**, **F%**, **G** et **G%** sont utilisés pour les arguments qui sont modifiés directement (modified-in-place). Lorsque les arguments **XLOPER** ou **XLOPER12** sont inscrits comme types **P** ou **Q** respectivement, Excel convertit les références à cellule unique en valeurs simples et les références à plusieurs cellules en tableaux lorsqu’il les prépare.
  
Les types **P** et **Q** arrivent toujours dans votre fonction sous la forme d’un des types suivants : **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeMissing**, or **xltypeNil**, mais pas **xltypeRef** ni **xltypeSRef**, car ceux-ci sont toujours déréférencés.
  
Le type **O**, qui représente réellement trois arguments sur la pile, a été introduit pour la compatibilité avec les DLL Fortran où les arguments sont passés par référence. Il ne peut pas être utilisé pour renvoyer une valeur sauf en déclarant l’argument comme une valeur de retour modify-in-place et en plaçant les résultats dans les valeurs référencées. Le type **O %** étend le type **O** dans Excel 2007 pour accéder aux tableaux couvrant des zones plus grandes que la grille Office Excel 2003.
  
## <a name="see-also"></a>Voir aussi

- [xlfRegister (formulaire 1)](xlfregister-form-1.md)
- [Concepts de programmation Excel](excel-programming-concepts.md)
- [Référence des fonctions XLL SDK API Excel 2013](excel-xll-sdk-api-function-reference.md)
