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
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e6430a54b0c0ed3b6e08d3c9256cae7dcde926ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19782207"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel appelle la [fonction xlAutoRegister](xlautoregister-xlautoregister12.md) chaque fois qu’un appel a été effectué pour la fonction XLM **inscrire**ou l' équivalent API C [fonction xlfRegister](xlfregister-form-1.md), avec les types de retour et l’argument de la fonction en cours d’enregistrement manquant. Il permet la ressource XLL à rechercher ses listes internes de fonctions exportées et commandes pour enregistrer la fonction avec l’argument et retournent des types spécifiés.
  
À compter d’Excel 2007, Excel appelle la fonction **xlAutoRegister12** plutôt que la fonction **xlAutoRegister** , si elle est exportée par la ressource XLL. 
  
Excel ne nécessite pas un ressource XLL à mettre en œuvre et exporter une de ces fonctions.
  
> [!NOTE]
> Si **xlAutoRegister**/ **xlAutoRegister12** tente d’inscrire la fonction sans fournir l’argument et types de retour, cet événement produit une boucle appelant récursive finalement de dépassement de la pile des appels et se bloque Excel. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Paramètres

 _pxName_ (**xltypeStr**)
  
Le nom de la fonction XLL qui est enregistré.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

La fonction doit renvoyer le résultat de la tentative d’inscrire le de fonction XLL _pxName_ à l’aide de la fonction **xlfRegister** . Si la fonction spécifiée ne fait pas partie des exportations du XLL, elle doit retourner la **#VALUE !** erreur ou **NULL** qui Excel interprète à **#VALUE !**.
  
## <a name="remarks"></a>Remarques

Votre implémentation de **xlAutoRegister** doit effectuer une recherche par le biais de listes internes de votre XLL des fonctions et des commandes qu'exporte vous recherchez une correspondance avec le nom passé pas la casse. Si la fonction ou la commande est trouvée, **xlAutoRegister** doit essayer de l’enregistrer à l’aide de la fonction **xlfRegister** , en veillant à fournir la chaîne qui indique les types de retour et l’argument de la fonction, ainsi que les autres requis à Excel informations sur la fonction. Il doit ensuite retourner vers Excel quelle que soit l’appel de **xlfRegister** renvoyé. Si la fonction a été enregistrée avec succès, **xlfRegister** renvoie une valeur de **xltypeNum** contenant l’ID de la fonction Enregistrer. 
  
### <a name="example"></a>Exemple

Consultez le fichier `SAMPLES\EXAMPLE\EXAMPLE.C` pour un exemple d’implémentation de cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[INSCRIRE](xlfregister-form-1.md)
  
[ANNULER L’INSCRIPTION](xlfunregister-form-1.md)

