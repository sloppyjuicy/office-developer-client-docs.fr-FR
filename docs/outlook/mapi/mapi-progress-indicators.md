---
title: Indicateurs de progression MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: cdfb6898146583b7da9b043eadd3acc09edbf292
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328209"
---
# <a name="mapi-progress-indicators"></a>Indicateurs de progression MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La plupart des opérations que vous effectuez pour les clients peuvent prendre beaucoup de temps. Pour informer les clients de la progression d'une opération longue, vous pouvez afficher un indicateur qui affiche sous forme graphique la partie terminée d'une opération à un moment donné, du début de l'opération à son achèvement. L'indicateur de progression indique un pourcentage de l'opération totale à effectuer.
  
Les méthodes suivantes prennent en charge les opérations longues et l'affichage d'un indicateur de progression:
  
- [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md), [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D Eletemessages](imapifolder-deletemessages.md), [IMAPIFolder::D Eletefolder](imapifolder-deletefolder.md), [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md)et [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md).
    
- [IMAPIProp:: CopyProps](imapiprop-copyprops.md) et [IMAPIProp:: CopyTo](imapiprop-copyto.md).
    
- [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md), [IMAPISupport::D ocopyto](imapisupport-docopyto.md), [IMAPISupport:: CopyFolder](imapisupport-copyfolder.md)et [IMAPISupport:: CopyMessages](imapisupport-copymessages.md).
    
- [IMessage::D eleteattach](imessage-deleteattach.md).
    
- [IABContainer:: CopyEntries](iabcontainer-copyentries.md).
    
Pour afficher un indicateur de progression, MAPI définit un objet de progression. Les objets Progress implémentent l'interface [méthode imapiprogress: IUnknown](imapiprogressiunknown.md) , une interface qui inclut des méthodes pour établir la plage de l'indicateur et créer l'affichage. MAPI fournit une implémentation d'objet de progression sous forme de clients. Vous devez utiliser l'implémentation d'un client, si elle est fournie, en tant que paramètre d'entrée de la méthode qui exécute l'opération. Si le client transmet NULL au lieu d'un pointeur vers un objet de progression, utilisez l'implémentation MAPI en appelant la méthode [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) . 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

