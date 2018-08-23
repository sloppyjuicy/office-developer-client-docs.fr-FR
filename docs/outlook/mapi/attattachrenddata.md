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
ms.openlocfilehash: a006c126ec5e0fb86847226195efd03f7ae5351f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569448"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
L’attribut **attAttachRenddata** est codé en une structure **RENDDATA** qui explique comment et où la pièce jointe est rendue dans le texte du message. La structure **RENDDATA** est simplement codée dans le flux TNEF sous forme d’octets **sizeof(RENDDATA)** commençant par le premier membre de la structure **RENDDATA** . Si la valeur du membre **dwFlags** de la structure **RENDDATA** est définie à **MAC_BINARY**, les données de la pièce jointe suivante sont stockées au format MacBinary ; dans le cas contraire, les données de la pièce jointe sont codées comme d’habitude.
  

