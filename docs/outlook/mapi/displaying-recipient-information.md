---
title: Affichage des informations du destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e1c31e5edf702dd8f172f67e7055a96ae4cfff1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337036"
---
# <a name="displaying-recipient-information"></a>Affichage des informations du destinataire

**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI fournit une boîte de dialogue commune pour afficher les détails des destinataires. La boîte de dialogue détails est créée à partir d'une table d'affichage et d'une implémentation **IMAPIProp** . Le tableau d'affichage décrit l'apparence de l'affichage des détails et l'implémentation **IMAPIProp** contrôle les données du destinataire. Votre fournisseur est responsable de la fourniture de la table d'affichage et de l'implémentation **IMAPIProp** pour chaque destinataire. 
  
Le moyen le plus simple de créer la table d'affichage consiste à définir une structure [DTPAGE](dtpage.md) et à appeler [BuildDisplayTable](builddisplaytable.md). Toutefois, certains fournisseurs, en particulier des fournisseurs en lecture seule qui permettent la création de destinataires uniques, utilisent **IPropData**. L'implémentation de **IMAPIProp** peut être n'importe quel type d'objet Property. 
  
Il existe deux méthodes pour appeler cette boîte de dialogue: [IAddrBook::D etails](iaddrbook-details.md) et [IMAPISupport::D etails](imapisupport-details.md). Lorsque votre fournisseur appelle l'une de ces méthodes pour demander les détails d'un destinataire, MAPI ouvre d'abord le destinataire en appelant la méthode [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) de son conteneur. Il appelle ensuite la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du destinataire pour demander la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). **PR_DETAILS_TABLE** est la propriété qui représente la table d'affichage des détails d'un destinataire. 
  
L'interface [IPropData: IMAPIProp](ipropdataimapiprop.md) peut être utilisée pour surveiller les modifications apportées aux contrôles d'affichage de table, comme décrit dans la procédure suivante. 
  
## <a name="monitor-changes-to-a-control"></a>Surveiller les modifications apportées à un contrôle
  
1. Avant que l'utilisateur n'accède au contrôle, appelez [IPropData:: HrSetObjAccess](ipropdata-hrsetobjaccess.md) pour définir l'accès du contrôle à IPROP_CLEAN. 
    
2. Autoriser l'utilisateur à travailler avec la boîte de dialogue. 
    
3. Lorsque l'utilisateur a terminé, appelez [IPropData:: HrGetPropAccess](ipropdata-hrgetpropaccess.md) pour récupérer le niveau d'accès actuel du contrôle. 
    
4. Si le niveau d'accès est IPROP_DIRTY, l'utilisateur a modifié le contrôle. Votre fournisseur doit:
    
   - Appelez [IPropData:: HrSetPropAccess](ipropdata-hrsetpropaccess.md) pour redéfinir le niveau d'accès sur IPROP_CLEAN. 
    
   - Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de l'objet de données de propriété pour extraire la propriété modifiée et la mettre à jour en appelant [IMAPIProp:: SetProps](imapiprop-setprops.md).
    
5. Si le niveau d'accès est toujours IPROP_CLEAN, le contrôle n'a pas été modifié. 
    
Pour plus d'informations sur la création de tables d'affichage, voir [afficher les tables](display-tables.md).
  

