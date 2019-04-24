---
title: DATE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Renvoie la date représentée par l'année, le mois et le jour mis en forme selon le format de date abrégée dans les paramètres régionaux du système. Les valeurs pour l'année, le mois et le jour reflètent le calendrier grégorien.
ms.openlocfilehash: 0175c1f06ec3dbdf89774759546c65994d38105e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360332"
---
# <a name="date-function-visioshapesheet"></a>DATE Function (VisioShapeSheet)

Renvoie la date représentée par l' *année, le mois* et le *jour* mis en forme selon le format de date abrégée dans les paramètres régionaux du système. Les valeurs pour l' *année*, le *mois* et le *jour* reflètent le calendrier grégorien. 
  
## <a name="syntax"></a>Syntaxe

DATE (* * *année* * *, * * *mois* * *, * * *jour* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _year_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Année  <br/> |
| _Mois_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Mois  <br/> |
| _day_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Jour  <br/> |
   
## <a name="example-1"></a>Exemple 1

DATE (1999, 6, 7)
  
Renvoie la valeur représentant le 07/06/99.
  
## <a name="example-2"></a>Exemple 2

DATE(1999;6;7) + 4 je.
  
Renvoie la valeur représentant 11/06/99.
  
## <a name="example-3"></a>Exemple 3

FORMAT (DATE (1999, 10, 14), «C»)
  
Renvoie la valeur représentant le mardi 14 octobre 1999.
  

