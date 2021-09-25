---
title: Indicateurs de progression MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d1317290b99fe3e10dec539e0a349382cc880188
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575644"
---
# <a name="mapi-progress-indicators"></a>Indicateurs de progression MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La plupart des opérations que vous effectuez pour les clients peuvent prendre beaucoup de temps. Pour informer les clients de la progression d’une opération longue, vous pouvez afficher un indicateur qui affiche graphiquement la partie terminée d’une opération à un moment donné depuis le début de l’opération jusqu’à son achèvement. L’indicateur de progression indique un pourcentage de l’opération totale à terminer.
  
Les méthodes suivantes supportent des opérations longues et l’affichage d’un indicateur de progression :
  
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::D eleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)et [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md), [IMAPISupport::D oCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)et [IMAPISupport::CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::D eleteAttach](imessage-deleteattach.md).
    
- [IABContainer::CopyEntries](iabcontainer-copyentries.md).
    
Pour afficher un indicateur de progression, MAPI définit un objet de progression. Les objets de progression implémentent l’interface [IMAPIProgress : IUnknown,](imapiprogressiunknown.md) une interface qui inclut des méthodes pour établir la plage de l’indicateur et créer l’affichage. MAPI fournit une implémentation d’objet de progression, tout comme certains clients. Vous devez utiliser l’implémentation d’un client, si elle est fournie, comme paramètre d’entrée pour la méthode qui exécute l’opération. Si le client transmet la valeur NULL au lieu d’un pointeur vers un objet de progression, utilisez l’implémentation de MAPI en appelant la méthode [IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md) 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

