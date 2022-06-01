---
title: Obtention de l’adresse e-mail d’un contact
description: Montre comment obtenir la valeur d’une propriété nommée qui représente l’adresse e-mail d’un élément Microsoft Outlook 2010 ou Microsoft Outlook 2013 Contact.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
ms.openlocfilehash: f0971c0edf99e948075457c785534c4eeeaa4c6a
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817500"
---
# <a name="get-the-email-address-of-a-contact-item"></a>Obtention de l’adresse e-mail d’un contact

**S’applique à** : Outlook 2013 | Outlook 2016
  
Cette rubrique montre comment obtenir la valeur d’une propriété nommée qui représente l’adresse e-mail d’un élément de contact Microsoft Outlook 2010 ou Microsoft Outlook 2013.
  
Vous pouvez associer jusqu’à trois adresses e-mail à un élément contact dans Outlook 2010 et Outlook 2013. Chaque adresse e-mail correspond à une propriété de l’objet **ContactItem** Outlook 2010 ou Outlook 2013 dans les modèles objet Outlook 2010 et Outlook 2013. Interne à Outlook 2010 et Outlook 2013, l’adresse e-mail correspond également à une propriété nommée MAPI. Par exemple, la première adresse e-mail d’un contact correspond à la propriété **Email1Address** de **ContactItem** dans les modèles objet Outlook 2010 et Outlook 2013, ainsi qu’à la propriété canonique Outlook 2010 et Outlook 2013 interne nommée [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).
  
Pour obtenir la valeur d’une adresse e-mail d’un élément de contact, vous pouvez utiliser l’objet **PropertyAccessor** du modèle objet Outlook 2010 ou Outlook 2013, ou d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété de la propriété nommée, puis spécifier cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l’appel **d’IMAPIProp::GetIDsFromNames**, spécifiez les valeurs appropriées pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d’entrée  _lppPropNames_. L’exemple de code suivant montre comment obtenir la première adresse e-mail d’un contact spécifié, lpContact', à l’aide de **GetIDsFromNames** et **GetProps**.
  
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
