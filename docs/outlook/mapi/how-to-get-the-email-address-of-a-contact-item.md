---
title: Obtenir l’adresse de messagerie d’un élément de Contact
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: ce9579cb6b07336cae7d69fe503c918d96946b0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783473"
---
# <a name="get-the-email-address-of-a-contact-item"></a>Obtenir l’adresse de messagerie d’un élément de Contact

**S’applique à**: Outlook 
  
Cette rubrique montre comment obtenir la valeur d’une propriété nommée qui représente l’adresse de messagerie d’un élément Microsoft Outlook 2010 ou de contacts Microsoft Outlook 2013.
  
Vous pouvez associer jusqu'à trois adresses de messagerie avec un élément de Contact dans Outlook 2010 et Outlook 2013. Chaque adresse de messagerie correspond à une propriété de l’objet Outlook 2010 ou Outlook 2013 **ContactItem** dans les modèles objet Outlook 2010 et Outlook 2013. Interne à Outlook 2010 et Outlook 2013, l’adresse de messagerie correspond à une propriété nommée de MAPI. Par exemple, la première adresse de messagerie d’un contact correspond à la propriété **Email1Address** de **ContactItem** dans les modèles objet Outlook 2010 et Outlook 2013 et le [nommé interne Outlook 2010 et Outlook 2013 Propriété canonique PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md).
  
Pour obtenir la valeur d’une adresse de messagerie d’un élément de contact, vous pouvez utiliser l’objet **PropertyAccessor** du modèle objet Outlook 2010 ou Outlook 2013, ou tout d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété de la propriété nommée, puis Spécifiez cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l’appel **IMAPIProp::GetIDsFromNames**, spécifiez les valeurs appropriées pour la structure [MAPINAMEID](mapinameid.md) sur laquelle pointé le paramètre d’entrée _lppPropNames_. L’exemple de code suivant montre comment obtenir la première adresse de messagerie d’un contact spécifique, `lpContact`, à l’aide de **GetIDsFromNames** et **GetProps**. 
  
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


