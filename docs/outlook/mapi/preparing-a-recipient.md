---
title: Préparation d’un destinataire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b4ccfb8cf8201a17993932acc4c0104ace80b94d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588719"
---
# <a name="preparing-a-recipient"></a>Préparation d’un destinataire

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une application cliente prépare les destinataires à convertir leurs identificateurs d’entrée à court terme identificateurs d’entrée à long terme et éventuellement l’ajout, modification ou réorganisation des propriétés. Vous pouvez préparer des destinataires qui font partie d’une liste de destinataires pour un message ou des destinataires qui ne sont pas liés à un message. En règle générale, les clients appeler [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directement pour convertir les identificateurs d’entrée à court terme en identificateurs d’entrée à long terme pour les destinataires qui sont inclus dans la boîte de dialogue adresses. Pour les destinataires qui sont associés à un message sortant, la préparation d’un destinataire est gérée par le processus de résolution de nom. 
  
Pour préparer une liste de destinataires, appelez **IAddrBook::PrepareRecips**. **PrepareRecips** accepte une structure [ADRLIST](adrlist.md) et une liste des balises de propriété. La structure **ADRLIST** contient les destinataires à préparer tandis que la liste de balise de propriété représente les propriétés de chaque destinataire doit prendre en charge. Tente de placer les propriétés qui sont incluses dans la liste de balise de propriété au début de la structure **ADRLIST** **PrepareRecips** . Si une des propriétés de la liste est manquante dans la structure **ADRLIST** , le fournisseur de carnet d’adresses pour fournir les appels MAPI. Si vous devez uniquement vérifier les identificateurs d’entrée à long terme, passez la valeur NULL pour le paramètre _lpSPropTagArray_ . 
  
Par exemple, supposons que vous travaillez avec des cinq destinataires. Tous les cinq destinataires apparaissent dans la structure **ADRLIST** avec les propriétés suivantes dans l’ordre suivant : 
  
1. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
2. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
3. **Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
4. **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
5. **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
Trois autres propriétés sont incluses dans la structure **ADRLIST** pour les deux premiers destinataires. 
  
1. **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))
    
2. **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))
    
3. **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))
    
Étant donné que tous les destinataires doivent avoir en tant que leurs trois premiers propriétés **TYPEADR_PR**, **PR_ENTRYID**et **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), créez un tableau de balise de propriété avec ces propriétés et le secret elle et la structure **ADRLIST** à **PrepareRecips**. **PrepareRecips** appelle la méthode **IMAPIProp::GetProps** de chaque destinataire pour récupérer **PR_HOME_TELEPHONE_NUMBER** , car il n’est pas partie de la structure **ADRLIST** . **PrepareRecips** retourne la liste des destinataires représente une liste de destinataires fusionnée avec les propriétés incluses dans la structure **ADRLIST** apparaissant en premier pour chaque destinataire. 
  
La liste de destinataires pour les destinataires 1 et 2 comprend des propriétés dans l’ordre suivant :
  
1. **TYPEADR_PR**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **ADRESSE_EMAIL_PR**
    
7. **TYPEADR_PR**
    
8. **PR_ACCOUNT**
    
9. **PR_GIVEN_NAME**
    
10. **PR_SURNAME**
    
La liste de destinataires pour les destinataires 3, 4 et 5 comprend des propriétés dans l’ordre suivant :
  
1. **TYPEADR_PR**
    
2. **PR_ENTRYID**
    
3. **PR_HOME_TELEPHONE_NUMBER**
    
4. **PR_DISPLAY_NAME**
    
5. **PR_SEARCH_KEY**
    
6. **ADRESSE_EMAIL_PR**
    
7. **TYPEADR_PR**
    
Comme alternative à l’appel **IAddrBook::PrepareRecips** pour utiliser des propriétés, appelez la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de chaque destinataire et, si nécessaire, la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) . Lorsque qu’un seul destinataire est impliqué, deux méthodes sont satisfaisants. Toutefois, lorsque plusieurs destinataires sont impliqués, l’appel **PrepareRecips** plutôt que les méthodes **IMAPIProp** gagne du temps et, si vous travaillez à distance, plusieurs appels de procédure distante. **PrepareRecips** traite tous les destinataires dans un seul appel tandis que **GetProps** et **SetProps** émettre un appel pour chaque destinataire. 
  

