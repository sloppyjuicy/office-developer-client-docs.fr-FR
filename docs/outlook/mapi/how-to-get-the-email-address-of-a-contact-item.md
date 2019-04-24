---
title: Obtention de l’adresse e-mail d’un contact
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: fab09d0c594bac1374973f523abe6ff0b9c09dd0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344687"
---
# <a name="get-the-email-address-of-a-contact-item"></a>Obtention de l’adresse e-mail d’un contact

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique montre comment obtenir la valeur d'une propriété nommée qui représente l'adresse de messagerie d'un élément de contact Microsoft Outlook 2010 ou Microsoft Outlook 2013.
  
Vous pouvez associer jusqu'à trois adresses de messagerie à un élément de contact dans Outlook 2010 et Outlook 2013. Chaque adresse de messagerie correspond à une propriété de l'objet Outlook 2010 ou Outlook 2013 **ContactItem** dans les modèles d'objet Outlook 2010 et Outlook 2013. En interne à Outlook 2010 et Outlook 2013, l'adresse de messagerie correspond également à une propriété nommée MAPI. Par exemple, la première adresse de messagerie d'un contact correspond à la propriété **Email1Address** de l'objet **ContactItem** dans les modèles d'objets outlook 2010 et Outlook 2013, et le nom interne outlook 2010 et Outlook 2013 nommé [ Propriété canonique PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md).
  
Pour obtenir la valeur d'une adresse de messagerie d'un contact, vous pouvez utiliser l'objet **propertyAccessor** du modèle objet Outlook 2010 ou Outlook 2013, ou utiliser d'abord [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété de la propriété nommée, puis Spécifiez cette balise de propriété dans [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l'appel de **IMAPIProp:: GetIDsFromNames**, spécifiez les valeurs appropriées pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d'entrée _lppPropNames_. L'exemple de code suivant montre comment obtenir la première adresse de messagerie d'un contact spécifié `lpContact`, à l'aide de **GetIDsFromNames** et de **GetProps**. 
  
```cpp
HRESULT HrGetEmail1(LPMESSAGE lpContact) 
{ 
    HRESULT hRes = S_OK; 
    LPSPropTagArray lpNamedPropTags = NULL; 
    MAPINAMEID NamedID = {0}; 
    LPMAPINAMEID lpNamedID = &NamedID; 
    NamedID.lpguid = (LPGUID)&PSETID_Address; 
    NamedID.ulKind = MNID_ID; 
    NamedID.Kind.lID = dispidEmailEmailAddress; 
 
    hRes = lpContact->GetIDsFromNames( 
           1,  
           &lpNamedID,  
           NULL,  
           &lpNamedPropTags); 
 
    if (SUCCEEDED(hRes) && lpNamedPropTags) 
    { 
        SPropTagArray sPropTagArray; 
 
        sPropTagArray.cValues = 1; 
        sPropTagArray.aulPropTag[0] = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[0],PT_STRING8); 
        LPSPropValue lpProps = NULL; 
        ULONG cProps = 0; 
 
        hRes = lpContact->GetProps( 
               &sPropTagArray, 
               NULL, 
               &cProps, 
               &lpProps); 
        if (SUCCEEDED(hRes) &&  
            1 == cProps &&  
            lpProps &&  
            PT_STRING8 == PROP_TYPE(lpProps[0].ulPropTag) && 
            lpProps[0].Value.lpszA) 
        { 
            printf("Email address 1 = \"%s\"\n",lpProps[0].Value.lpszA); 
        } 
        MAPIFreeBuffer(lpProps); 
        MAPIFreeBuffer(lpNamedPropTags); 
     } 
     return hRes; 
}
```


