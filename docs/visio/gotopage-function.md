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
description: Affiche la page qui contient le nom pagename dans la fenêtre actuellement active.
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397148"
---
# <a name="gotopage-function"></a>Fonction GOTOPAGE

Affiche la page qui contient le nom *pagename* dans la fenêtre actuellement active. 
  
## <a name="syntax"></a>Syntaxe

GOTOPAGE (« ** *pagename* ** ») 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _pagename_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Nom de la page à atteindre  <br/> |
   
## <a name="remarks"></a>Remarques

Si une fenêtre est déjà la page, cette fenêtre devient active. Si *pagename* n’existe pas, l’application tente d’accéder à https:// *pagename* /. Si Visio opère comme un serveur sur place, la fonction GOTOPAGE n’a aucun effet. 
  
Vous pouvez utiliser la fonction HYPERLINK pour accéder à n’importe quel chemin DOS, UNC ou URL. 
  
Dans les versions précédentes de Visio, cette fonction s’appelait _GOTOPAGE. Les versions Visio 4.0 et ultérieures acceptent l’un ou l’autre style. 
  

