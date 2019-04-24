---
title: Problèmes connus dans Excel XLL Development
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- problèmes connus [Excel 2007]
localization_priority: Normal
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 34784f6895386efe7e6c3ca7ec213c7d71931058
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304003"
---
# <a name="known-issues-in-excel-xll-development"></a>Problèmes connus dans Excel XLL Development

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Cette rubrique décrit les problèmes connus dans Microsoft Excel que vous pouvez rencontrer dans le développement d'XLL.
  
## <a name="unregistering-xll-commands-and-functions"></a>Annulation de l'inscription des fonctions et des commandes XLL

Lorsqu'une XLL enregistre une fonction ou une commande, Excel crée un nouveau nom pour la ressource et associe une référence à la fonction DLL portant ce nom. Le nom provient du quatrième argument, *pxFunctionText* , de la fonction [xlfRegister](xlfregister-form-1.md) . Ce nom est masqué dans les boîtes de dialogue normales de gestion des noms de feuille de calcul. Pour annuler l'inscription d'une fonction ou commande, vous devez supprimer le nom à l'aide de la fonction [xlfSetName](xlfsetname.md) , en transmettant le nom, mais sans lui transmettre de définition. Toutefois, un bogue l'empêche de supprimer le nom de la liste de l'Assistant function. 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>Troncation de chaîne de description d'argument dans l'Assistant de fonction

Le paramètre *pxArgumentHelp1* et tous les paramètres suivants de la fonction **xlfRegister** sont des chaînes facultatives qui correspondent aux arguments de la fonction XLL. L'Assistant fonction affiche ces éléments pour fournir de l'aide dans la boîte de dialogue construction des arguments. Parfois, Excel tronque la chaîne qui correspond à l'argument final par un ou deux caractères lors de son affichage dans la boîte de dialogue. Vous pouvez éviter cela en ajoutant une «chaîne vide» supplémentaire en tant que dernier paramètre «aide sur les arguments» de votre inscription de fonction.
  
## <a name="binary-name-scope-limitation"></a>Limite d'étendue de nom binaire

Les noms binaires et leurs données ne peuvent être récupérés que lorsque la feuille de calcul qui était active au moment de sa création est de nouveau active. Étant donné que les fonctions de feuille de calcul ne peuvent pas activer les feuilles de calcul dans un classeur (seules les commandes peuvent le faire), les applications de noms binaires sont très limitées. Si vous avez une commande qui est appelée uniquement à partir d'une feuille de calcul particulière, par exemple, vous pouvez utiliser un nom binaire pour stocker les données liées aux commandes.
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>xlSet et classeurs avec des formules matricielles

Dans Excel 2003 et les versions antérieures, la [fonction xlSet](xlset.md) échoue si vous essayez d'affecter des valeurs à une plage dans une feuille de calcul qui n'est pas la feuille de calcul active, où la plage équivalente de la feuille active contient une formule matricielle. Dans ce cas, Excel affiche le message «vous ne pouvez pas modifier une partie d'un tableau». Cela a été résolu dans Excel 2007. 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>Les références circulaires sont tolérées dans les tables de données

Excel ne génère pas d'erreur pour l'instant si le calcul basé sur une table de données fait référence à un élément du tableau lui-même. Comme ce scénario peut être improbable, soyez prudent lorsque vous créez ou modifiez des formules utilisées pour calculer des valeurs de tables de données.
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>Conversion d'un entier XLOPER12 en une valeur XLOPER

Étant donné que le type d'entier **xltypeInt** est un entier signé de 32 bits dans le type de données **XLOPER12** , mais qu'il ne s'agit que d'un entier signé 16 bits dans le type de données **XLOPER** , il est possible que certaines valeurs de la variable **XLOPER12** entière ne puissent pas être contenues dans une type **XLOPER**entier. Lorsque Excel convertit ce type en interne, il contourne ce problème en convertissant le type en un XLOPER **xltypeNum** **** en virgule flottante.
  
La fonction [XLOper12ToXLOper](xloper12toxloper.md) de l'infrastructure met en miroir ce comportement pour être cohérent avec Excel en interne. Lorsque vous appelez cette fonction, vous ne devez pas supposer que l' **XLOPER** renvoyée sera toujours **xltypeInt**; la lecture de **my_xloper. Val. w** renvoie une valeur false si le type **my_xloper** est **xltypeNum**.
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>Renvoi d'XLOPER ou de XLOPER12 en modifiant des arguments sur place

Excel autorise l'inscription des fonctions qui renvoient une structure **XLOPER** ou **XLOPER12** en modifiant un argument sur place. Toutefois, si un argument **XLOPER XLOPER**/ **** pointe vers la mémoire et que le pointeur est remplacé par la valeur de retour de la fonction dll, Excel peut entraîner une fuite de mémoire. Excel n'affiche pas d'erreur, mais peut finir par se bloquer. En outre, si la DLL alloue de la mémoire pour la valeur de retour, Excel peut essayer de libérer cette mémoire, ce qui peut entraîner un blocage immédiat de l'application. Par conséquent, vous ne devez ****/ pas modifier les arguments de la section**XLOPER12** . Tous les arguments **XLOPER** ou **XLOPER12** doivent être traités comme étant strictement en lecture seule. 
  
Pour plus d�informations, voir [Gestion de la m�moire dans Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Voir aussi



[XLOper12ToXLOper](xloper12toxloper.md)


[D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)
  
[R�f�rence des fonctions XLL SDK API Excel 2013](excel-xll-sdk-api-function-reference.md)
  
[Gestion de la m�moire dans Excel](memory-management-in-excel.md)

