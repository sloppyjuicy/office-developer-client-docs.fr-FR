---
title: Problèmes connus dans le développement Excel XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- problèmes connus [excel 2007]
ms.localizationpriority: medium
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
ms.openlocfilehash: 3d7a1a5bb3e3344e985c17706a4f0d8c3b4ec1e9
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198848"
---
# <a name="known-issues-in-excel-xll-development"></a>Problèmes connus dans le développement Excel XLL

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio
  
Cette rubrique décrit les problèmes connus dans Microsoft Excel que vous pourriez rencontrer dans le développement XLL.
  
## <a name="unregistering-xll-commands-and-functions"></a>Désinssion des fonctions et des commandes XLL

Lorsqu’un XLL inscrit une fonction ou une commande, Excel crée un nouveau nom pour la ressource et associe une référence à la fonction DLL à ce nom. Le nom est tiré du quatrième argument, *pxFunctionText*, de la [fonction xlfRegister.](xlfregister-form-1.md) Ce nom est masqué dans les boîtes de dialogue normales pour la gestion des noms de feuille de calcul. Pour désinsister une fonction ou une commande, vous devez supprimer le nom à l’aide de la fonction [xlfSetName,](xlfsetname.md) en passant le nom sans passer de définition. Toutefois, un bogue empêche cette suppression du nom des listes de l’Assistant Fonction.
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>Troncation de chaîne de description d’argument dans l’Assistant Fonction

Le *paramètre pxArgumentHelp1*  et tous les paramètres suivants de la fonction **xlfRegister** sont des chaînes facultatives qui correspondent aux arguments de la fonction XLL. L’Assistant Fonction les affiche pour fournir de l’aide dans la boîte de dialogue de construction des arguments. Parfois, Excel tronque la chaîne qui correspond à l’argument final d’un ou deux caractères lors de son affichage dans la boîte de dialogue. Vous pouvez éviter cela en ajoutant une « chaîne vide » supplémentaire comme dernier paramètre « aide de l’argument » de l’inscription de votre fonction.
  
## <a name="binary-name-scope-limitation"></a>Limite d’étendue du nom binaire

Les noms binaires et leurs données ne peuvent être récupérés que lorsque la feuille de calcul active au moment de leur création est de nouveau active. Étant donné que les fonctions de feuille de calcul ne peuvent pas activer les feuilles de calcul dans un workbook (seules les commandes peuvent le faire), les applications de noms binaires sont très limitées. Si vous avez une commande qui est uniquement invoquée à partir d’une feuille de calcul particulière, par exemple, vous pouvez utiliser un nom binaire pour stocker des données liées aux commandes.
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>XlSet et workbooks avec formules ma matrice

Dans Excel 2003 et versions antérieures, la fonction [xlSet](xlset.md) échoue si vous essayez d’affecter des valeurs à une plage d’une feuille de calcul qui n’est pas la feuille de calcul active, où la plage équivalente de la feuille active contient une formule ma matrice. Dans ce cas, Excel affiche le message « Vous ne pouvez pas modifier une partie d’un tableau ». Cette situation a été corrigée Excel 2007.
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>Les références circulaires sont tolérables dans les tables de données

Excel ne renvoie actuellement pas d’erreur si le calcul d’une table de données fait référence à un objet de la table elle-même. Aussi peu probable que ce scénario puisse l’être, soyez prudent lorsque vous créez ou modifiez des formules utilisées pour calculer des valeurs de table de données.
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>Conversion d’un xlOPER12 d’un integer en XLOPER

Étant donné que le type d’ensemble **xltypeInt** est un nombre integer signé 32 bits dans le type de données **XLOPER12,** mais qu’il ne s’agit que d’un nombre unique signé 16 bits dans le type de données **XLOPER,** il est possible que certaines valeurs **XLOPER12** d’un nombre d’un nombre integer ne peuvent pas être contenues dans un nombre d’nombres **xlOPER**. Lorsque Excel convertit ce type en interne, il permet de contourner ce problème en convertissant le type en **xltypeNum** XLOPER à pointe **flottante.**
  
La fonction [Framework XLOper12ToXLOper](xloper12toxloper.md) reflète ce comportement pour être cohérente avec Excel interne. Lorsque vous appelez cette fonction, vous ne devez pas supposer que la **XLOPER** renvoyée sera **toujours xltypeInt**; reading **my_xloper.val.w** donne une valeur false si le type **my_xloper** est **xltypeNum**.
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>Renvoi de XLOPER ou XLOPER12 en modifiant les arguments sur place

Excel permet l’inscription des fonctions qui retournent une **XLOPER** ou **XLOPER12** en modifiant un argument en place. Toutefois, si un argument /  **XLOPER XLOPER12** pointe vers la mémoire et que le pointeur est ensuite remplacé par la valeur de retour de la fonction DLL, Excel la mémoire peut être divulguée. Excel n’affiche pas d’erreur, mais peut se crasher. En outre, si la DLL a alloué de la mémoire pour la valeur de retour, Excel pouvez essayer de libérer cette mémoire, ce qui peut provoquer un arrêt immédiat de l’application. Par conséquent, vous ne devez pas modifier les /  arguments **XLOPER XLOPER12** en place. Tous les arguments **XLOPER** ou **XLOPER12** doivent être traités comme étant strictement en lecture seule.
  
Pour plus d’informations, reportez-vous à la rubrique [Gestion de la mémoire dans Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Voir aussi

[XLOper12ToXLOper](xloper12toxloper.md) 
 [Développement Excel XLS](developing-excel-xlls.md)  
[Référence des fonctions XLL SDK API Excel 2013](excel-xll-sdk-api-function-reference.md)  
[Gestion de la mémoire dans Excel](memory-management-in-excel.md)