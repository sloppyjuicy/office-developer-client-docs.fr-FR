---
title: UNICHAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Renvoie le caractère Unicode à partir d’un nombre.
ms.openlocfilehash: 06f97717ee4d5965253b0da7cfd5c35faf0ca2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789973"
---
# <a name="unichar-function"></a>UNICHAR, fonction

Renvoie le caractère Unicode à partir d’un nombre. 
  
## <a name="syntax"></a>Syntaxe

UNICHAR (** *numéro* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Integer** <br/> |Entier compris entre 1 et 65 535 (inclus), ou la fonction renvoie une erreur.  <br/> |
   
## <a name="remarks"></a>Note

La chaîne obtenue présente une longueur d’un caractère unicode (deux caractères). 
  
## <a name="example"></a>Exemple

UNICHAR (65) 
  
Renvoie un (LETTRE MAJUSCULE LATINE A) 
  

