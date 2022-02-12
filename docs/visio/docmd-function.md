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
ms.openlocfilehash: cd9cae4a9c5c50b5a12dd86466f88a58bae578b1
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62774404"
---
# <a name="docmd-function"></a>Fonction DOCMD

Exécute la commande identifiée.
  
## <a name="syntax"></a>Syntaxe

 **DOCMD**( _commandID_)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _commandID_ <br/> |Requis  <br/> |**Number** <br/> | Commande à exécuter |
   
## <a name="remarks"></a>Remarques

Pour obtenir la liste des commandes qui sont pris en charge avec la fonction DOCMD, voir la rubrique « Commandes DoCmd/DOCMD » dans microsoft Visio 2013 Automation Reference. 
  
## <a name="example"></a>Exemple

 `DOCMD (1312)`
  
Entraîne l’affichage de la boîte de dialogue **Données de forme** dans l’interface utilisateur. 
  

