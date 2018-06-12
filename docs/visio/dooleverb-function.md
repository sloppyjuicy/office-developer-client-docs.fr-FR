---
title: DOOLEVERB, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
localization_priority: Normal
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: Exécute un verbe de l’objet OLE.
ms.openlocfilehash: a7786c3ef2b4039e288596ed367083a4ed3a6c13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788507"
---
# <a name="dooleverb-function"></a>DOOLEVERB, fonction

Exécute un verbe de l’objet OLE.
  
## <a name="syntax"></a>Syntaxe

DOOLEVERB (« ** *verbe* ** ») 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _« verbe »_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Verbe à exécuter  <br/> |
   
## <a name="remarks"></a>Note

Dans les versions précédentes de Visio, cette fonction s’appelait _DOOLEVERB. Les versions Visio 4.0 et ultérieures acceptent l’un ou l’autre style. 
  
## <a name="example"></a>Exemple

DOOLEVERB("modifier")
  
Exécute le programme de l’objet OLE et affiche l’objet lié ou imbriqué pour qu’il puisse être modifié.
  

