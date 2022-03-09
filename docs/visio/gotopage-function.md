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
ms.openlocfilehash: 9330f978866256262a12e8bc0049fa3690b5461d
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404389"
---
# <a name="gotopage-function"></a>Fonction GOTOPAGE

Affiche la page dont le nom est  *nom dans*  la fenêtre active.
  
## <a name="syntax"></a>Syntaxe

GOTOPAGE( » ***pagename*** « )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *pagename* <br/> |Requis  <br/> |**String** <br/> |Nom de la page à atteindre |

## <a name="remarks"></a>Remarques

Si la page est déjà ouverte dans une fenêtre, cette fenêtre est activée. Si *le nom de page n’existe* pas, l’application tente d’accéder https://  *pagename*  /. Si Visio opère comme un serveur de modification sur place, la fonction GOTOPAGE n’a aucun effet.
  
Vous pouvez utiliser la fonction HYPERLINK pour accéder à n’importe quel chemin DOS, UNC ou URL.
  
Dans les versions précédentes de Visio, cette fonction s’appelait _GOTOPAGE. Les versions Visio 4.0 et ultérieures acceptent l’un ou l’autre style.
  