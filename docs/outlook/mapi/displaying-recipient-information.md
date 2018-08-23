---
title: Affichage des informations sur les destinataires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4610d9e643541e39144f2af86a2d64928b8e9ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591288"
---
# <a name="displaying-recipient-information"></a>Affichage des informations sur les destinataires

**S’applique à**: Outlook 2013 | Outlook 2016 
  
MAPI fournit une boîte de dialogue pour afficher des détails sur le destinataires. La boîte de dialogue Détails est créée à partir d’un tableau d’affichage et une implémentation **IMAPIProp** . Le tableau de l’affichage décrit l’apparence de l’affichage des détails et l’implémentation **IMAPIProp** contrôle les données pour le destinataire. Votre fournisseur est chargé de fournir le tableau d’affichage et l’implémentation **IMAPIProp** pour chaque destinataire. 
  
Pour créer la table d’affichage le plus simple consiste à définir une structure [DTPAGE](dtpage.md) et appelez [BuildDisplayTable](builddisplaytable.md). Toutefois, certains fournisseurs, spécifiquement fournisseurs en lecture seule qui permettent la création de destinataires uniques, utilisent **IPropData**. L’implémentation **IMAPIProp** peut être n’importe quel type d’objet property. 
  
Il existe deux méthodes pour l’appel de cette boîte de dialogue : [IAddrBook::Details](iaddrbook-details.md) et [IMAPISupport::Details](imapisupport-details.md). Lorsque votre fournisseur appelle une de ces méthodes pour demander les détails pour un destinataire, MAPI commence par le destinataire en appelant la méthode de [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) de son conteneur. Il appelle ensuite la méthode de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du destinataire pour demander la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** est la propriété qui représente la table affichage de détails d’un destinataire. 
  
La [IPropData : IMAPIProp](ipropdataimapiprop.md) interface peut être utilisée pour surveiller les modifications sur les contrôles d’affichage de tableau comme décrit dans la procédure suivante. 
  
## <a name="monitor-changes-to-a-control"></a>Surveiller les modifications à un contrôle
  
1. Avant que l’utilisateur accède au contrôle, appelez [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) pour définir l’accès au contrôle IPROP_CLEAN. 
    
2. Autoriser l’utilisateur à l’utilisation de la boîte de dialogue. 
    
3. Lorsque l’utilisateur a terminé, appelez [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) pour récupérer le niveau d’accès actuel du contrôle. 
    
4. Si le niveau d’accès est IPROP_DIRTY, l’utilisateur a modifié le contrôle. Votre fournisseur doit :
    
   - Appelez [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) pour définir l’accès au niveau au IPROP_CLEAN. 
    
   - Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’objet de données de propriété pour récupérer la propriété modifiée et le mettre à jour en appelant [IMAPIProp::SetProps](imapiprop-setprops.md).
    
5. Si le niveau d’accès est toujours IPROP_CLEAN, le contrôle n’a pas été modifié. 
    
Pour plus d’informations sur la création de tableaux d’affichage, voir [Afficher les Tables](display-tables.md).
  

