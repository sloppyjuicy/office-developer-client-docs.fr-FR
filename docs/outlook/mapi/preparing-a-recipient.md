---
title: Préparation d'un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419876"
---
# <a name="preparing-a-recipient"></a>Préparation d'un destinataire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une application cliente prépare les destinataires en convertissant leurs identificateurs d'entrée à court terme en identificateurs d'entrée à long terme et éventuellement en ajoutant, en modifiant ou en réorganisant des propriétés. Vous pouvez préparer des destinataires qui font partie d'une liste de destinataires pour un message ou des destinataires qui ne sont pas liés à un message. En règle générale, les clients appellent [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) directement pour traduire des identificateurs d'entrée à court terme dans des identificateurs d'entrée à long terme pour les destinataires inclus dans la boîte de dialogue adresse commune. Pour les destinataires associés à un message sortant, la préparation des destinataires est gérée par le processus de résolution de noms. 
  
Pour préparer une liste de destinataires, appelez **IAddrBook::P reparerecips**. **PrepareRecips** accepte une structure [ADRLIST](adrlist.md) et une liste de balises de propriété. La structure **ADRLIST** contient les destinataires à préparer tandis que la liste des balises de propriétés représente les propriétés que chaque destinataire doit prendre en charge. **PrepareRecips** tente de placer les propriétés qui sont incluses dans la liste de balises de propriété au début de la structure **ADRLIST** . Si certaines propriétés de la liste sont absentes de la structure **ADRLIST** , MAPI appelle le fournisseur de carnet d'adresses pour les fournir. Si vous devez uniquement vérifier les identificateurs d'entrée à long terme, transmettez la valeur NULL pour le paramètre _lpSPropTagArray_ . 
  
Par exemple, supposons que vous travaillez avec cinq destinataires. Les cinq destinataires s'affichent dans la structure **ADRLIST** avec les propriétés suivantes dans l'ordre suivant: 
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
Trois autres propriétés sont incluses dans la structure **ADRLIST** pour les deux premiers destinataires. 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
Étant donné que tous les destinataires doivent avoir les trois premières propriétés **PR_ADDRTYPE**, **PR_ENTRYID**et **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), créez un tableau de balises de propriété avec ces propriétés et transmettez et la structure **ADRLIST** à **PrepareRecips**. **PrepareRecips** appelle la méthode **IMAPIProp:: GetProps** de chaque destinataire pour extraire **PR_HOME_TELEPHONE_NUMBER** car elle ne fait actuellement pas partie de la structure **ADRLIST** . Lorsque **PrepareRecips** renvoie, la liste de destinataires représente une liste fusionnée de destinataires avec les propriétés incluses dans la structure **ADRLIST** apparaissant en premier pour chaque destinataire. 
  
La liste des destinataires 1 et 2 des destinataires inclut des propriétés dans l'ordre suivant:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
8. **PR_ACCOUNT**
    
9. **PR_GIVEN_NAME**
    
10. **PR_SURNAME**
    
La liste des destinataires pour les destinataires 3, 4 et 5 inclut des propriétés dans l'ordre suivant:
  
1. **PR_ADDRTYPE**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **PR_EMAIL_ADDRESS**
    
7. **PR_ADDRTYPE**
    
En guise d'alternative à l'appel de **IAddrBook::P reparerecips** pour utiliser les propriétés, appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de chaque destinataire et, si nécessaire, sa méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) . Lorsqu'un seul destinataire est impliqué, l'une ou l'autre technique est satisfaisante. Toutefois, lorsque plusieurs destinataires sont impliqués, le fait d'appeler **PrepareRecips** plutôt que les méthodes **IMAPIProp** permet de gagner du temps et, si vous utilisez à distance, de nombreux appels de procédure distante. **PrepareRecips** traite tous les destinataires dans un appel unique, tandis que **GetProps** et **SetProps** effectuent un appel pour chaque destinataire. 
  

