---
title: Indicateurs de progression MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8fc39c6d7da0970ee15cdd9dd67bfeef0997d7d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582867"
---
# <a name="mapi-progress-indicators"></a>Indicateurs de progression MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
De nombreuses opérations que vous effectuez pour les clients peuvent prendre beaucoup de temps. Pour informer les clients de la progression d’une longue opération, vous pouvez afficher un indicateur qui affiche sous forme graphique la partie d’une opération terminée à un moment donné à partir du début de l’opération à la fin. L’indicateur de progression indique un pourcentage du total l’opération se termine.
  
Les méthodes suivantes prennent en charge les opérations de longue durée et l’affichage d’un indicateur de progression :
  
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)et [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md) et [IMAPIProp::CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)et [IMAPISupport::CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::DeleteAttach](imessage-deleteattach.md).
    
- [IABContainer::CopyEntries](iabcontainer-copyentries.md).
    
Pour afficher un indicateur de progression, MAPI définit un objet de progression. Implémentent des objets de l’avancement du [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, une interface qui inclut des méthodes pour l’établissement de la plage de l’indicateur et de création de l’affichage. MAPI fournit une implémentation d’objet de progression comme certains clients. Vous devez utiliser la mise en œuvre d’un client, le cas échéant, comme paramètre d’entrée à la méthode effectue l’opération. Si le client transmet NULL au lieu d’un pointeur vers un objet de progression, utilisez la mise en œuvre de MAPI en appelant la méthode [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) . 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

