---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- fonction fdance [excel 2007]
ms.localizationpriority: medium
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
ms.openlocfilehash: d38f16f007ae9ad9189971883a195fb9f7bbf4ee
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198904"
---
# <a name="fdance"></a>fDance

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple de commande définie par l’utilisateur qui modifie les cellules sélectionnées dans la feuille de calcul active jusqu’à ce que l’utilisateur appuie sur **ÉCHAP**. Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, Generic, via lequel cette commande est accessible.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Paramètres

La fonction ne prend aucun paramètre.
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de renvoi

La fonction renvoie toujours 1.
  
## <a name="remarks"></a>Remarques

Il s’agit d’un exemple d’une opération longue. Il appelle parfois la fonction [xlAbort.](xlabort.md) Cela permet au processeur (d’aider à la multitâche multinationale) et de vérifier si l’utilisateur a appuyer sur **ÉCHAP** pour annuler l’opération. Si c’est le cas, il offre à l’utilisateur la possibilité d’annuler l’abandon. 
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions dans le fichier DLL générique](functions-in-the-generic-dll.md)

