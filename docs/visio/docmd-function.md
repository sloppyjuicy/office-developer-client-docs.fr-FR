---
title: DOCMD, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
ms.localizationpriority: medium
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Exécute la commande identifiée.
ms.openlocfilehash: b6ab817dd437cd844bab4662fbb76f6921cd36a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628450"
---
# <a name="docmd-function"></a>Fonction DOCMD

Exécute la commande identifiée.
  
## <a name="syntax"></a>Syntaxe

 **DOCMD**( _commandID_)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _commandID_ <br/> |Obligatoire  <br/> |**Number** <br/> | Commande à exécuter  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir la liste des commandes qui sont pris en charge avec la fonction DOCMD, voir la rubrique « Commandes DoCmd/DOCMD » dans microsoft Visio 2013 Automation Reference. 
  
## <a name="example"></a>Exemple

 `DOCMD (1312)`
  
Entraîne l’affichage de la boîte de dialogue **Données de forme** dans l’interface utilisateur. 
  

