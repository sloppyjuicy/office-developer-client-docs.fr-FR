---
title: Problèmes connus concernant le développement de XLL Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- problèmes connus [excel 2007]
localization_priority: Normal
ms.assetid: 3dfecc0b-a91c-448e-8721-5d3486b625fa
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34784f6895386efe7e6c3ca7ec213c7d71931058
ms.sourcegitcommit: f139451a43598b59da22775333779df691df460a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2018
ms.locfileid: "26685178"
---
# <a name="known-issues-in-excel-xll-development"></a>Problèmes connus concernant le développement de XLL Excel

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Cette rubrique décrit les problèmes connus dans Microsoft Excel que vous pouvez rencontrer dans le développement de XLL.
  
## <a name="unregistering-xll-commands-and-functions"></a>Annulation de l’inscription commandes XLL et fonctions

Lorsqu’un XLL enregistre une commande ou une fonction, Excel crée un nouveau nom pour la ressource et l’associe une référence à la fonction DLL portant ce nom. Le nom est extrait du quatrième argument, *pxFunctionText* , de la fonction [xlfRegister](xlfregister-form-1.md) . Ce nom est masqué dans les boîtes de dialogue normal pour la gestion des noms de feuille de calcul. Pour annuler l’inscription d’une fonction ou une commande, vous devez supprimer le nom en utilisant la fonction [xlfSetName](xlfsetname.md) , en passant le nom mais ne pas en passant une définition. Toutefois, un bogue les empêche de supprimer le nom de l’Assistant fonction listes. 
  
## <a name="argument-description-string-truncation-in-the-function-wizard"></a>Troncation de chaîne argument Description dans l’Assistant fonction

Le paramètre *pxArgumentHelp1* et tous les paramètres suivants de la fonction **xlfRegister** sont facultatifs chaînes qui correspondent aux arguments de la fonction XLL. L’Assistant fonction affiche ces pour fournir plus d’informations sur la boîte de dialogue construction argument. Parfois, Excel tronque la chaîne qui correspond à l’argument final d’un ou deux caractères lors de son affichage dans la boîte de dialogue. Vous pouvez éviter cela en ajoutant une « chaîne vide » supplémentaire en tant que le dernier paramètre « aide argument » de l’enregistrement de fonction.
  
## <a name="binary-name-scope-limitation"></a>Limitation d’étendue nom binaire

Noms binaires et les données peuvent être récupérées uniquement lorsque la feuille de calcul qui était active au moment qu'ils ont été créés redevient actif. Étant donné que les fonctions de feuille de calcul ne peuvent pas activer des feuilles de calcul dans un classeur (seuls les commandes possible), des noms binaires sont très limitées. Par exemple, si vous avez une commande qui est appelée uniquement à partir d’une feuille de calcul, vous pouvez utiliser un nom binaire pour stocker les données associées à une commande.
  
## <a name="xlset-and-workbooks-with-array-formulas"></a>Classeurs avec des formules matricielles et xlSet

Dans Excel 2003 et versions antérieures, la [fonction xlSet](xlset.md) échoue si vous essayez d’affecter des valeurs à une plage dans une feuille de calcul qui n’est pas la feuille de calcul active, où la plage équivalente sur la feuille active contient une formule matricielle. Dans ce cas, Excel affiche le message « Impossible de modifier une partie d’un tableau. » Ce problème est résolu dans Excel 2007. 
  
## <a name="circular-references-are-tolerated-in-data-tables"></a>Références circulaires sont tolérées dans les Tables de données

Excel actuellement sans générer une erreur si le calcul basé sur une table de données fait référence à un élément dans le tableau proprement dit. Probable que ce scénario pourrait être, soyez prudent quand vous créez ou modifiez les formules qui sont utilisés pour calculer les valeurs de table de données.
  
## <a name="converting-an-integer-xloper12-to-an-xloper"></a>Convertir un XLOPER12 entier un XLOPER

Étant donné que le type de nombre entier **xltypeInt** est un entier signé 32 bits dans le type de données **XLOPER12** , mais il est uniquement un entier signé 16 bits dans le type de données **XLOPER** , il est possible que certaines valeurs de **XLOPER12** entier ne peut pas être inclus dans un nombre entier **XLOPER**. Où Excel convertit ce type en interne, il obtient à convertir le type d’une virgule flottante **xltypeNum** **XLOPER**résoudre ce problème.
  
La fonction Framework [XLOper12ToXLOper](xloper12toxloper.md) reflète ce comportement pour qu’il soit compatible avec Excel en interne. Lorsque vous appelez cette fonction, vous ne devez pas considérer que le renvoyée **XLOPER** sera toujours **xltypeInt**; lecture **my_xloper.val.w** donne la valeur false si le type de **my_xloper** est **xltypeNum**.
  
## <a name="returning-xloper-or-xloper12-by-modifying-arguments-in-place"></a>Renvoi XLOPER ou XLOPER12 en modifiant les Arguments en Place

Excel autorise l’inscription des fonctions qui retournent un **XLOPER** ou les **XLOPER12** en modifiant un argument en place. Toutefois, si un **XLOPER**/ **XLOPER12** argument points à la mémoire et le pointeur est ensuite remplacé par la valeur de retour de la fonction DLL, Excel peut une fuite de mémoire. Excel n’affiche pas une erreur, mais il peut se bloquer par la suite. En outre, si la DLL alloué pour la valeur de retour de la mémoire, Excel peut essayer de Libérez de la mémoire, qui peut entraîner un arrêt immédiat des applications. Par conséquent, vous ne devez pas modifier **XLOPER**/ arguments**XLOPER12** en place. **XLOPER** ou **XLOPER12** de tous les arguments doivent être traités comme strictement en lecture seule. 
  
Pour plus d�informations, voir [Gestion de la m�moire dans Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Voir aussi



[XLOper12ToXLOper](xloper12toxloper.md)


[Développement de XLL de Excel 2013](developing-excel-xlls.md)
  
[Référence des fonctions XLL SDK API Excel 2013](excel-xll-sdk-api-function-reference.md)
  
[Gestion de la mémoire dans Excel](memory-management-in-excel.md)

