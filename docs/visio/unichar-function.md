---
title: UNICHAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
ms.localizationpriority: medium
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Renvoie le caractère Unicode d’un nombre.
ms.openlocfilehash: 8f37e4890b785a0b3557efc1167dc80868f72c7a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603220"
---
# <a name="unichar-function"></a>Fonction UNICHAR

Renvoie le caractère Unicode d’un nombre. 
  
## <a name="syntax"></a>Syntaxe

UNICHAR (** *nombre* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Entier compris entre 1 et 65 535 (inclus), ou la fonction renvoie une erreur.  <br/> |
   
## <a name="remarks"></a>Remarques

La chaîne obtenue présente une longueur d’un caractère unicode (deux caractères). 
  
## <a name="example"></a>Exemple

UNICHAR(65) 
  
Renvoie A (lettre majuscule latine A) 
  

