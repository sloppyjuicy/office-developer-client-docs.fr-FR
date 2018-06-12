---
title: Fonction DATE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Renvoie la date représentée par année, mois et jour formatée en fonction de la date abrégée défini dans les paramètres régionaux du système. Les valeurs de l’année, mois et jour conformes au calendrier grégorien.
ms.openlocfilehash: 7a19d97f70f9314ecdbd2228078e1e18b1ac9146
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788435"
---
# <a name="date-function-visioshapesheet"></a>Fonction DATE (VisioShapeSheet)

Renvoie la date représentée par *année, mois* et *jour* formatée en fonction de la date abrégée défini dans les paramètres régionaux du système. Les valeurs de *l’année*, *mois* et *jour* conformes au calendrier grégorien. 
  
## <a name="syntax"></a>Syntaxe

DATE (** *année* **, ** *mois* **, ** *jour* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _year_ <br/> |Obligatoire  <br/> |**Integer** <br/> |Année  <br/> |
| _Mois_ <br/> |Obligatoire  <br/> |**Integer** <br/> |Mois  <br/> |
| _day_ <br/> |Obligatoire  <br/> |**Integer** <br/> |Jour  <br/> |
   
## <a name="example-1"></a>Exemple 1

DATE(1999;6;7)
  
Renvoie la valeur représentant le 07/06/99.
  
## <a name="example-2"></a>Exemple 2

DATE(1999;6;7) + 4 je.
  
Renvoie la valeur représentant 11/06/99.
  
## <a name="example-3"></a>Exemple 3

FORMAT(DATE(1999;10;14);"C")
  
Renvoie la valeur représentant le mardi 14 octobre 1999.
  

