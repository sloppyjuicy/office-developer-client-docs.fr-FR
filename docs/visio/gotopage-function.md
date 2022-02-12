---
title: GOTOPAGE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
ms.localizationpriority: medium
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: Affiche la page dont le nom est nom dans la fenêtre active.
ms.openlocfilehash: 735871c5090c7d6fc2d3fd41eb4318d084932a77
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62778551"
---
# <a name="gotopage-function"></a>Fonction GOTOPAGE

Affiche la page dont le nom est  *nom dans*  la fenêtre active. 
  
## <a name="syntax"></a>Syntaxe

GOTOPAGE( » ** *pagename* ** « ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _pagename_ <br/> |Requis  <br/> |**String** <br/> |Nom de la page à atteindre |
   
## <a name="remarks"></a>Remarques

Si la page est déjà ouverte dans une fenêtre, cette fenêtre est activée. Si  *le nom de page n’existe*  pas, l’application tente d’accéder https://  *pagename*  /. Si Visio opère comme un serveur de modification sur place, la fonction GOTOPAGE n’a aucun effet. 
  
Vous pouvez utiliser la fonction HYPERLINK pour accéder à n’importe quel chemin DOS, UNC ou URL. 
  
Dans les versions précédentes de Visio, cette fonction s’appelait _GOTOPAGE. Les versions Visio 4.0 et ultérieures acceptent l’un ou l’autre style. 
  

