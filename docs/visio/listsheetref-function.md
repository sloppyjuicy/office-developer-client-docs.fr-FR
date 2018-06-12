---
title: LISTSHEETREF, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 87ddbc35-8577-0a96-20b8-aa7734764c5b
description: Renvoie une référence de feuille à la forme conteneur de liste qui contient la forme.
ms.openlocfilehash: 75c765fab2d287c2da83a659dbbf070d29a9d325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788996"
---
# <a name="listsheetref-function"></a>LISTSHEETREF, fonction

Renvoie une référence de feuille à la forme conteneur de liste qui contient la forme.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010 
  
## <a name="syntax"></a>Syntaxe

LISTMEMBERCOUNT()
  
### <a name="return-value"></a>Valeur renvoy�e

Référence ShapeSheet
  
## <a name="remarks"></a>Note

Si la forme n’est pas un membre de la liste, la fonction LISTSHEETREF renvoie #REF!.
  
## <a name="example"></a>Exemple

LISTSHEETREF(1)!Height 
  
Renvoie la valeur de la cellule Height de la forme conteneur de liste qui contient la forme. 
  

