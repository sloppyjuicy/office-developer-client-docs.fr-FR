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
description: Renvoie la date représentée par l’année, le mois et le jour formatés en fonction du style de date courte dans l’Paramètres du système. Les valeurs de l’année, du mois et du jour reflètent le calendrier grégorien.
ms.openlocfilehash: 83b704a55e145f50d685c6dc9dde9d838dda9e8f
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770470"
---
# <a name="date-function-visioshapesheet"></a>DATE Function (VisioShapeSheet)

Renvoie la date représentée par l’année *,* le mois  et le jour formatés en fonction du style de date courte dans l’Paramètres du système. Les valeurs  *de l’année*, *du mois*  et  *du*  jour reflètent le calendrier grégorien. 
  
## <a name="syntax"></a>Syntaxe

DATE(** *year* **, ** *month* **, ** *day* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _year_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Année |
| _Mois_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Mois |
| _day_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Jour |
   
## <a name="example-1"></a>Exemple 1

DATE(1999,6,7)
  
Renvoie la valeur représentant le 07/06/99.
  
## <a name="example-2"></a>Exemple 2

DATE(1999;6;7) + 4 je.
  
Renvoie la valeur représentant 11/06/99.
  
## <a name="example-3"></a>Exemple 3

FORMAT(DATE(1999,10,14),"C »)
  
Renvoie la valeur représentant le mardi 14 octobre 1999.
  

