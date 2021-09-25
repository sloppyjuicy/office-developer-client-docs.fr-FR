---
title: DATE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
ms.localizationpriority: medium
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Renvoie la date représentée par l’année, le mois et le jour formatés en fonction du style de date courte dans les Paramètres du système. Les valeurs de l’année, du mois et du jour reflètent le calendrier grégorien.
ms.openlocfilehash: 820329bbe9283cae540625d4232d4095c6a1a530
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577905"
---
# <a name="date-function-visioshapesheet"></a>DATE Function (VisioShapeSheet)

Renvoie la date représentée par l’année, le mois et le jour formatés en fonction du style de date courte dans le Paramètres du système.   Les valeurs  *de l’année,* *du mois*  et du  *jour*  reflètent le calendrier grégorien. 
  
## <a name="syntax"></a>Syntaxe

DATE(** *year* **, ** *month* **, ** *day* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _year_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Année  <br/> |
| _Mois_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Mois  <br/> |
| _day_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Jour  <br/> |
   
## <a name="example-1"></a>Exemple 1

DATE(1999,6,7)
  
Renvoie la valeur représentant le 07/06/99.
  
## <a name="example-2"></a>Exemple 2

DATE(1999;6;7) + 4 je.
  
Renvoie la valeur représentant 11/06/99.
  
## <a name="example-3"></a>Exemple 3

FORMAT(DATE(1999,10,14),"C »)
  
Renvoie la valeur représentant le mardi 14 octobre 1999.
  

