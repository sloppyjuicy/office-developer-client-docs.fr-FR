---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- fonction xlAutoRegister [Excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303947"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel appelle la [fonction xlAutoRegister](xlautoregister-xlautoregister12.md) chaque fois qu'un appel a été passé à la **** fonction XLM, ou à la [fonction xlfRegister](xlfregister-form-1.md)de l'API C, avec les types de retour et d'argument de la fonction inscrite manquants. Elle permet à la XLL d'effectuer des recherches dans ses listes internes de fonctions et de commandes exportées pour enregistrer la fonction avec l'argument et les types de retour spécifiés.
  
À partir d'Excel 2007, Excel appelle la fonction **xlAutoRegister12** de préférence à la fonction **xlAutoRegister** si elle est exportée par le XLL. 
  
Excel ne nécessite pas de XLL pour implémenter et exporter l'une ou l'autre de ces fonctions.
  
> [!NOTE]
> Si **xlAutoRegister**/ **xlAutoRegister12** tente d'inscrire la fonction sans fournir les types d'argument et de retour, une boucle d'appel récursive a lieu, ce qui finit par déborder la pile des appels et provoquer l'arrêt d'Excel. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Paramètres

 _pxName_ (**xltypeStr**)
  
Nom de la fonction XLL en cours d'enregistrement.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La fonction doit renvoyer le résultat de la tentative d'enregistrement de la fonction XLL _pxName_ à l'aide de la fonction **xlfRegister** . Si la fonction spécifiée n'est pas l'une des exportations de la XLL, elle doit renvoyer le **#VALUE!** erreur ou **valeur null** qu'Excel interprète sur **#VALUE!**.
  
## <a name="remarks"></a>Remarques

Votre implémentation de **xlAutoRegister** doit effectuer une recherche ne respectant pas la casse dans les listes internes de votre XLL des fonctions et des commandes qu'elle exporte en recherchant une correspondance avec le nom transmis. Si la fonction ou commande est trouvée, **xlAutoRegister** doit essayer de l'enregistrer, à l'aide de la fonction **xlfRegister** , en veillant à fournir la chaîne qui indique à Excel les types de retour et d'argument de la fonction, ainsi que les autres informations sur la fonction. Elle doit ensuite retourner à Excel tout en renvoyant l'appel à **xlfRegister** . Si la fonction a été enregistrée, **xlfRegister** renvoie une valeur **XLTYPENUM** contenant l'ID de la fonction. 
  
### <a name="example"></a>Exemple

Pour obtenir un `SAMPLES\EXAMPLE\EXAMPLE.C` exemple d'implémentation de cette fonction, consultez le fichier. 
  
## <a name="see-also"></a>Voir aussi



[CASIER](xlfregister-form-1.md)
  
[ANNULER l'inscription](xlfunregister-form-1.md)

