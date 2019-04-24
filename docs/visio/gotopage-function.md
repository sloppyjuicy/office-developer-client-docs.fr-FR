---
title: GOTOPAGE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
localization_priority: Normal
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: Affiche la page portant le nom nompage dans la fenêtre active.
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302967"
---
# <a name="gotopage-function"></a>Fonction GOTOPAGE

Affiche la page portant le nom *nompage* dans la fenêtre active. 
  
## <a name="syntax"></a>Syntaxe

GOTOPAGE ("* * *pagename* * *") 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _pagename_ <br/> |Obligatoire  <br/> |**String** <br/> |Nom de la page à atteindre  <br/> |
   
## <a name="remarks"></a>Remarques

Si la page est déjà ouverte dans une fenêtre, cette fenêtre est activée. Si *pagename* n'existe pas, l'application tente d'accéder à https:// *pagename* /. Si Visio opère comme un serveur de modification sur place, la fonction GOTOPAGE n’a aucun effet. 
  
Vous pouvez utiliser la fonction HYPERLINK pour accéder à n’importe quel chemin DOS, UNC ou URL. 
  
Dans les versions précédentes de Visio, cette fonction s’appelait _GOTOPAGE. Les versions Visio 4.0 et ultérieures acceptent l’un ou l’autre style. 
  

