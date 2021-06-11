---
title: Prise en charge de texte mis en forme  Rendu des pi�ces jointes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68abe85b-5dc0-40d0-8917-30ea002aa816
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5f03530f994fd13e7dc4c7eaa4124900c28e613b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405295"
---
# <a name="supporting-formatted-text-rendering-attachments"></a>Prise en charge du texte formaté : rendu des pièces jointes

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une application cliente qui se soucie de l’endroit où sont rendues ses pièces jointes dans un message définit la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) pour ces pièces jointes pendant la composition du message. Un client qui ne se soucie pas placement de rendu laisse cette propri�t� non d�finie.
  
Lorsqu'un client ouvre un message contenant des pi�ces jointes, il tente de r�cup�rer la propri�t� de **PR_RENDERING_POSITION** de chaque pi�ce jointe afin de d�terminer o� la pi�ce jointe doit �tre affich�e dans le texte du message. Un client peut utiliser une des m�thodes suivantes pour r�cup�rer **PR_RENDERING_POSITION**:
  
- [IMAPIProp::GetProps](imapiprop-getprops.md) on the open attachment to retrieve the **PR_RENDERING_POSITION** property. 
    
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) on the open message to retrieve its attachment table. **PR_RENDERING_POSITION** is a required column in all attachment tables. This is the preferred method because it results in better performance. 
    
Banques de messages prenant en charge au format RTF peuvent choisir s'il faut retourner une valeur exacte ou approximative pour **PR_RENDERING_POSITION**. �tant donn� que les banques de messages recalculer valeur de **PR_RENDERING_POSITION** d'une pi�ce jointe lorsque vous �tes invit� pour la propri�t� du message **PR_BODY**, certains messages RTF prenant en charge stocke uniquement les garantie la pr�cision du rendu positionne lorsqu'un client demande d'abord **PR_BODY**. Banques de messages prenant en charge au format RTF sont autoris�s � fournir aux clients ayant des valeurs de position de rendu approximatif pour am�liorer les performances. Fournissant une approximative plut�t qu'une position de rendu pr�cis gagne du temps et est suffisant pour la plupart des cas. 
  
Banques de messages RTF prenant en charge doivent reposer leur rapprochement de la valeur sp�cifi�e par le client responsable de la cr�ation de la pi�ce jointe. Bien que tous les clients doivent d�finir **PR_RENDERING_POSITION**, les fournisseurs de banque de message doivent �tre pr�ts � traiter avec la possibilit� de son absence. Lorsque le client ne d�finit pas **PR_RENDERING_POSITION**, une banque de messages peut lui attribuer -1 pour indiquer que la position de rendu n'est pas dans le texte du message. Les pi�ces jointes avec une position de rendu de la valeur -1 peuvent �tre affich�s � n'importe quel endroit au sein du message en fonction du client. De nombreux clients positionner ces types de pi�ces jointes en haut du message.
  
Le degré de précision d’une propriété **PR_RENDERING_POSITION** varie selon qu’une boutique de messages enregistre ou non les propriétés **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) ou uniquement **PR_RTF_COMPRESSED**. Si le client g�n�re **PR_BODY** et que la banque de messages enregistre en m�me temps que le texte mis en forme, les positions de rendu seront pr�cises. Toutefois, si la banque de messages doit g�n�rer sa propre version de **PR_BODY**, car il enregistre uniquement **PR_RTF_COMPRESSED**, il est probable que les positions de rendu sera un peu impr�cises. Il s'agit en raison des diff�rences dans la mani�re dont que les clients et les fournisseurs de banque de messages g�n�rent la propri�t� **PR_BODY**. 
  
To calculate an accurate **PR_RENDERING_POSITION** value, an RTF-aware store uses a tag embedded in the formatted text. The utility function **RTFSync** can be called to perform this calculation and update an attachment's rendering position. Depending on the amount of state information available, the message store can pass either RTF_SYNC_BODY_CHANGED, RTF_SYNC_RTF_CHANGED, or both values to [RTFSync](rtfsync.md).
  

