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
description: Renvoie la date représentée par l’année, le mois et le jour formatés en fonction du style de date courte dans le Paramètres du système. Les valeurs de l’année, du mois et du jour reflètent le calendrier grégorien.
ms.openlocfilehash: 2ed3e34f85f2262062ee6514bd4855611a07e32b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381942"
---
# <a name="date-function-visioshapesheet"></a>DATE Function (VisioShapeSheet)

Renvoie la date représentée par l’année *,* le mois  et le jour formatés en fonction du style de date courte dans l’Paramètres du système. Les valeurs *de l’année*, *du mois* et *du jour* reflètent le calendrier grégorien.
  
## <a name="syntax"></a>Syntaxe

DATE(***year** _, _*_month_*_, _*_day_**)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *year* <br/> |Obligatoire  <br/> |**Entier** <br/> |Année |
| *Mois* <br/> |Obligatoire  <br/> |**Entier** <br/> |Mois |
| *day* <br/> |Obligatoire  <br/> |**Entier** <br/> |Jour |

## <a name="example-1"></a>Exemple 1

DATE(1999,6,7)
  
Renvoie la valeur représentant le 07/06/99.
  
## <a name="example-2"></a>Exemple 2

DATE(1999;6;7) + 4 je.
  
Renvoie la valeur représentant 11/06/99.
  
## <a name="example-3"></a>Exemple 3

FORMAT(DATE(1999,10,14),"C »)
  
Renvoie la valeur représentant le mardi 14 octobre 1999.
  