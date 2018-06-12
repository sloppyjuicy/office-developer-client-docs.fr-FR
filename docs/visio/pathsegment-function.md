---
title: PATHSEGMENT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Renvoie le numéro de segment de base 1 à la marque de pourcentage spécifiée le long du chemin d’accès spécifié.
ms.openlocfilehash: b25f43ffa3c719cfc5ffbd1e417f2da9640e483b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789232"
---
# <a name="pathsegment-function"></a>PATHSEGMENT, fonction

Renvoie le numéro de segment de base 1 à la marque de pourcentage spécifiée le long du chemin d’accès spécifié.
  
## <a name="syntax"></a>Syntaxe

PATHSEGMENT (** *section* **, ** *voyage* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).  <br/> |
| _frais de déplacement_ <br/> |Obligatoire  <br/> |**Double** <br/> |Pourcentage du chemin parcouru du point de début au point de fin. La valeur doit être comprise entre 0 et 1.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Entier
  

