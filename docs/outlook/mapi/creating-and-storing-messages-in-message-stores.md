---
title: Cr�ation et le stockage des Messages dans les banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: be718ea3ef4da91d2f85a0229f5a506198a2527f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589174"
---
# <a name="creating-and-storing-messages-in-message-stores"></a>Cr�ation et le stockage des Messages dans les banques de messages

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Comment votre fournisseur de banque de messages cr�e et stocke les messages dans le m�canisme de stockage sous-jacent d�pendent essentiellement le m�canisme de stockage sous-jacent lui-m�me. En r�gle g�n�rale, vous devez uniquement d'�crire du code afin de pr�server les propri�t�s d'un message et leurs valeurs.
  
Lors de la banque de messages fournisseur cr�e un nouveau message, le fournisseur a besoin cr�er le message avec les propri�t�s requises pour les messages. Vous trouverez une liste de ces propri�t�s dans la documentation relative � la [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface. Apr�s cela, les applications clientes ajouter des propri�t�s suppl�mentaires avec les m�thodes [IMAPIProp](imapipropiunknown.md) . 
  
Lors de la banque de messages fournisseur enregistre un message dans le m�canisme de stockage sous-jacent, le fournisseur a besoin effectuer une it�ration sur les propri�t�s de message, puis enregistrez-les dans le m�canisme de stockage sous-jacent, tels qu'ils peuvent �tre enti�rement r�cup�r�s si le message est ouvert par la suite.
  
MAPI exige que les propri�t�s sur les interfaces [IMessage](imessageimapiprop.md) sont trait�es, ce qui signifie que les modifications apport�es � leur ne sont pas d�finitive jusqu'� ce que la m�thode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appel�e sur l'objet du message. Le fournisseur de banque de messages est responsable de l'impl�mentation de ce comportement. Cela n'est g�n�ralement pas difficile ; Cela signifie simplement que contenant des propri�t�s en m�moire pendant qu'ils sont en cours de modification et les rendre permanentes dans le m�canisme de stockage sous-jacent lorsque **SaveChanges** est appel�e. 
  
Certaines propri�t�s d'objets de message ont une s�mantique sp�ciale pour les applications clientes par rapport � la m�thode **SaveChanges**, comme suit : 
  
- Certaines propri�t�s doivent �tre en lecture/�criture avant **SaveChanges** est appel�e, mais en lecture seule par la suite. Par exemple, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) est définie à l’origine par l’application cliente qui crée le message (et par conséquent est en lecture/écriture), mais ne peut pas être modifié après le premier appel à **SaveChanges**.
    
- Certaines propri�t�s ont des relations particuli�res aux propri�t�s sur le dossier qu'ils sont dans ou aux m�thodes de **IMAPIFolder**. Par exemple, la propri�t� **PR_MESSAGE_FLAGS** est li�e aux indicateurs utilis�s lors de l'appel de [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . 
    
- Certaines propri�t�s ne soient pas disponibles tant que **SaveChanges** est appel� pour la premi�re fois. Par exemple, la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) sera ne peut-être pas disponible avant **SaveChanges** est appelée. 
    
- Certaines propri�t�s peuvent avoir des relations sp�ciales � d'autres propri�t�s sur l'objet du message. Par exemple, la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) est généralement dérivée de la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) dans les fournisseurs de magasins de message qui prennent en charge des messages au Format RTF.
    
- Certaines propri�t�s sont utilis�es par plusieurs types d'objet associ�s aux magasins de message. Par exemple, la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) est requis sur le dossier et les objets ainsi que message stocker des objets de message.
    
Il est de la responsabilit� du fournisseur de banque de messages pour impl�menter la s�mantique appropri�e pour ces propri�t�s.
  
## <a name="see-also"></a>Voir aussi



[L'impl�mentation des Messages dans les banques de messages](implementing-messages-in-message-stores.md)

