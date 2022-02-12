---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e6d63b5025fba8c9a0028fcda1f8395f55441352
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781491"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un identificateur d’entrée pour une adresse unique.
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpszName_
  
> [in] Pointeur vers la valeur de la propriété **PR_DISPLAY_NAME (**[PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du destinataire. Le  _paramètre lpszName_ peut être NULL. 
    
 _lpszAdrType_
  
> [in] Pointeur vers le type d’adresse du destinataire, tel que FAX ou SMTP. Le  _paramètre lpszAdrType_ ne peut pas être NULL. 
    
 _lpszAddress_
  
> [in] Pointeur vers l’adresse du destinataire. Le  _paramètre lpszAddress_ ne peut pas être NULL. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui affecte le destinataire. Les indicateurs suivants peuvent être définies :
    
MAPI_SEND_NO_RICH_INFO 
  
> Le destinataire ne peut pas gérer le contenu des messages formatés. Si MAPI_SEND_NO_RICH_INFO est définie, MAPI définit la propriété **PR_SEND_RICH_INFO (**[PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) du destinataire sur FALSE. Si MAPI_SEND_NO_RICH_INFO n’est pas définie, MAPI définit cette propriété sur TRUE, sauf si l’adresse de messagerie du destinataire pointée par  _lpszAddress_ est interprétée comme une adresse Internet. Dans ce cas, MAPI **définit PR_SEND_RICH_INFO** sur FALSE. 
    
MAPI_UNICODE 
  
> Le nom complet, le type d’adresse et l’adresse sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, ces chaînes sont au format ANSI.
    
 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’byte dans l’identificateur d’entrée pointé par  _le paramètre lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée du destinataire unique.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’identificateur d’entrée unique a été créé avec succès.
    
## <a name="remarks"></a>Remarques

Les clients appellent la méthode **CreateOneOff** pour créer un identificateur d’entrée pour un destinataire unique , un destinataire qui n’appartient à aucun des conteneurs des fournisseurs de carnet d’adresses actuellement chargés. Les destinataires non professionnels peuvent avoir n’importe quel type d’adresse pris en charge par l’un des fournisseurs de carnets d’adresses actifs pour la session. 
  
Les destinataires spécifiques sont généralement créés avec un modèle pour leur type d’adresse particulier. Le fournisseur de carnet d’adresses qui prend en charge le type d’adresse fournit le modèle. Un utilisateur d’une application cliente entre les informations pertinentes dans le modèle.
  
MAPI prend en charge les chaînes de caractères Unicode pour le nom d’affichage, le type d’adresse et les paramètres d’adresse **de CreateOneOff**.
  
L MAPI_SEND_NO_RICH_INFO contrôle si le texte formaté au format RTF (Rich Text Format) est envoyé avec chaque message. Le format TNEF (Transport Neutral Encapsulation Format), un format utilisé pour transmettre du texte formaté, est envoyé par la plupart des fournisseurs de transport, quelle que soit la façon dont le destinataire définit sa propriété **PR_SEND_RICH_INFO** . Ce n’est pas un problème pour les clients de messagerie qui travaillent avec des messages interpersonnels. Toutefois, étant donné que le TNEF est généralement utilisé pour envoyer des propriétés personnalisées pour des classes de message personnalisées, le fait de ne pas le prendre en charge peut être un problème pour les clients basés sur un formulaire ou les clients qui nécessitent des propriétés MAPI personnalisées. Pour plus d’informations, voir [Sending Messages with TNEF](sending-messages-with-tnef.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI utilise la **méthode CreateOneOff** pour créer un ID d’entrée pour une adresse qui n’est trouvée dans aucun carnet d’adresses. |
   
## <a name="see-also"></a>Voir aussi



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

