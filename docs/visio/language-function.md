---
title: LANGUAGE Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Autorise les opérations de comparaison entre différentes représentations de langue. Il est préférable de convertir les valeurs de balises de langue IETF (Internet Engineering Task Force) en valeurs d'ID de paramètres régionaux (LCID).
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327817"
---
# <a name="language-function"></a>LANGUAGE Function

Autorise les opérations de comparaison entre différentes représentations de langue. Il est préférable de convertir les valeurs de balises de langue IETF (Internet Engineering Task Force) en valeurs d'ID de paramètres régionaux (LCID).
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013
 
  
## <a name="syntax"></a>Syntaxe

 **Langue** ( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Obligatoire  <br/> |**String** <br/> |Valeur LCID ou BCP 47 de la langue.  <br/> |
   
## <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="example"></a>Exemple

 `LANGUAGE("en-us")`
  
Renvoie la valeur «1033».
  
 `LANGUAGE("es-es")`
  
Renvoie la valeur «3082».
  

