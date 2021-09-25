---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a21f6ca242f07abf865885794cf71f0ff3135eba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605173"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
**L’attribut attAttachRenddata** est codé en tant que structure **RENDDATA** qui décrit comment et où la pièce jointe est restituer dans le texte du message. La structure **RENDDATA** est simplement codée dans le flux TNEF en tant qu’octets **sizeof(RENDDATA)** commençant par le premier membre de la structure **RENDDATA.** Si la valeur du membre **dwFlags** de la structure **RENDDATA** est définie sur **MAC_BINARY**, les données de la pièce jointe suivante sont stockées au format MacBinary ; Dans le cas contraire, les données de pièce jointe sont codées comme d’habitude.
  

