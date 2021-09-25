---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- fonction xlautoregister [excel 2007]
ms.localizationpriority: medium
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c43a6248e3d9bb06bcc07c1629846d135b909f5f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557581"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel appelle la fonction [xlAutoRegister](xlautoregister-xlautoregister12.md) chaque fois qu’un appel a été effectué à la fonction XLM **REGISTER** ou à la fonction [xlfRegister](xlfregister-form-1.md)équivalente à l’API C, les types de retour et d’argument de la fonction étant manquants. Il permet au XLL de rechercher ses listes internes de fonctions et de commandes exportées pour enregistrer la fonction avec l’argument et les types de retour spécifiés.
  
À partir Excel 2007, Excel appelle la fonction **xlAutoRegister12** de préférence à la fonction **xlAutoRegister** si elle est exportée par le XLL. 
  
Excel ne nécessite pas de XLL pour implémenter et exporter l’une de ces fonctions.
  
> [!NOTE]
> Si **xlAutoRegister** /  **xlAutoRegister12** tente d’inscrire la fonction sans fournir les types d’argument et de retour, une boucle d’appel récursive se produit, ce qui finit par déborder la pile d’appels et se Excel. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Paramètres

 _pxName_ (**xltypeStr**)
  
Nom de la fonction XLL en cours d’inscription.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La fonction doit renvoyer le résultat de la tentative d’inscription de la fonction _XLL pxName_ à l’aide de la **fonction xlfRegister.** Si la fonction spécifiée n’est pas l’une des exportations du XLL, elle doit renvoyer le **#VALUE!** error, or **NULL** which Excel will interpret at **#VALUE!**.
  
## <a name="remarks"></a>Remarques

Votre implémentation de **xlAutoRegister** doit effectuer une recherche sans prendre en compte la cas dans les listes internes de votre XLL des fonctions et commandes qu’il exporte à la recherche d’une correspondance avec le nom transmis. Si la fonction ou la commande est trouvée, **xlAutoRegister** doit tenter de l’enregistrer à l’aide de la fonction **xlfRegister,** en vous assurez de fournir la chaîne qui indique à Excel les types de retour et d’argument de la fonction, ainsi que toute autre information requise sur la fonction. Il doit ensuite revenir à Excel quel que soit l’appel **à xlfRegister** renvoyé. Si la fonction a été enregistrée avec succès, **xlfRegister** renvoie une valeur **xltypeNum** contenant l’ID d’inscription de la fonction. 
  
### <a name="example"></a>Exemple

Consultez le fichier  `SAMPLES\EXAMPLE\EXAMPLE.C` pour obtenir un exemple d’implémentation de cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[REGISTER](xlfregister-form-1.md)
  
[UNREGISTER](xlfunregister-form-1.md)

