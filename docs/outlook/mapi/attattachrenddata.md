---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d58fc0eae5401773d28f5bbe510913ff381ade8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427135"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'attribut **attAttachRenddata** est encodé sous la forme d'une structure **RENDDATA** qui décrit comment et où la pièce jointe est affichée dans le texte du message. La structure **RENDDATA** est simplement codée dans le flux TNEF en tant qu'octets **sizeof (RENDDATA)** en commençant par le premier membre de la structure **RENDDATA** . Si la valeur du membre **dwFlags** de la structure **RENDDATA** est définie sur **MAC_BINARY**, les données de la pièce jointe suivante sont stockées dans le format MacBinary; dans le cas contraire, les données de la pièce jointe sont codées comme d'habitude.
  

