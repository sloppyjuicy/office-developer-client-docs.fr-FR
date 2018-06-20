---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d8c6699ac1bc5687b1c885d156535e5b54b93140
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782953"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**S’applique à**: Outlook 
  
L’attribut **attAttachRenddata** est codé en une structure **RENDDATA** qui explique comment et où la pièce jointe est rendue dans le texte du message. La structure **RENDDATA** est simplement codée dans le flux TNEF sous forme d’octets **sizeof(RENDDATA)** commençant par le premier membre de la structure **RENDDATA** . Si la valeur du membre **dwFlags** de la structure **RENDDATA** est définie à **MAC_BINARY**, les données de la pièce jointe suivante sont stockées au format MacBinary ; dans le cas contraire, les données de la pièce jointe sont codées comme d’habitude.
  

