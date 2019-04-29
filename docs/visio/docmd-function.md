---
title: DOCMD, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
localization_priority: Normal
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Exécute la commande identifiée.
ms.openlocfilehash: 9e5c02c9a90f3aab66c5d582c83d7d9d892f964c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413072"
---
# <a name="docmd-function"></a>Fonction DOCMD

Exécute la commande identifiée.
  
## <a name="syntax"></a>Syntaxe

 **DoCmd** ( _CommandID_)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _CommandID_ <br/> |Obligatoire  <br/> |**Number** <br/> | Commande à exécuter  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir la liste des commandes prises en charge par la fonction DOCMD, voir la rubrique relative aux commandes DoCmd/DOCMD dans la référence d'Automation de Microsoft Visio 2013. 
  
## <a name="example"></a>Exemple

 `DOCMD (1312)`
  
Entraîne l’affichage de la boîte de dialogue **Données de forme** dans l’interface utilisateur. 
  

