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
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b7a2fbdf723d06dcf9b02789178d7d12d0515884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782129"
---
# <a name="fdance"></a>fDance

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemple définies par l’utilisateur de commande qui modifie des cellules sélectionnées autour de la feuille de calcul active jusqu'à ce que l’utilisateur appuie sur **ÉCHAP**. Lorsque GENERIC.xll est chargé, il crée un menu défini par l’utilisateur, générique, par le biais de laquelle cette commande est accessible.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Paramètres

La fonction ne prend aucun paramètre.
  
## <a name="property-valuereturn-value"></a>Propriété valeur/valeur de retour

La fonction renvoie toujours 1.
  
## <a name="remarks"></a>Remarques

Il s’agit d’un exemple d’une longue opération. Il appelle la fonction [xlAbort](xlabort.md) occasionnellement. Cela donne le processeur (aident à multitâche coopératif) et vérifie si l’utilisateur a appuyé sur **ÉCHAP** pour annuler l’opération. Dans ce cas, il offre à l’utilisateur d’annuler l’abandon. 
  
### <a name="example"></a>Exemple

Voir `\SAMPLES\GENERIC\GENERIC.C` pour le code source pour cette fonction. 
  
## <a name="see-also"></a>Voir aussi



[Fonctions de la DLL générique](functions-in-the-generic-dll.md)

