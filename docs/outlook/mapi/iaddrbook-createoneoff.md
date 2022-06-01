---
title: IAddrBookCreateOneOff
description: Cet article décrit la fonction IAddrBookCreateOneOff et fournit la syntaxe, les paramètres et la valeur de retour.
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
ms.openlocfilehash: e3655b08ec40aed08fe6c62b171b058b95bec042
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815792"
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
  
> [in] Pointeur vers la valeur de la propriété **PR_DISPLAY_NAME** du destinataire ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Le paramètre  _lpszName_ peut être NULL. 
    
 _lpszAdrType_
  
> [in] Pointeur vers le type d’adresse du destinataire, tel que FAX ou SMTP. Le paramètre  _lpszAdrType_ ne peut pas être NULL. 
    
 _lpszAddress_
  
> [in] Pointeur vers l’adresse du destinataire. Le paramètre  _lpszAddress_ ne peut pas être NULL. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui affecte le destinataire unique. Les indicateurs suivants peuvent être définis :
    
MAPI_SEND_NO_RICH_INFO 
  
> Le destinataire ne peut pas gérer le contenu du message mis en forme. Si MAPI_SEND_NO_RICH_INFO est défini, MAPI définit la propriété **PR_SEND_RICH_INFO** du destinataire ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) sur FALSE. Si MAPI_SEND_NO_RICH_INFO n’est pas définie, MAPI définit cette propriété sur TRUE, sauf si l’adresse de messagerie du destinataire pointée par  _lpszAddress_ est interprétée comme une adresse Internet. Dans ce cas, MAPI définit **PR_SEND_RICH_INFO** sur FALSE. 
    
MAPI_UNICODE 
  
> Le nom d’affichage, le type d’adresse et l’adresse sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, ces chaînes sont au format ANSI.
    
 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée pour le destinataire unique.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’identificateur d’entrée unique a été créé avec succès.
    
## <a name="remarks"></a>Remarques

Les clients appellent la méthode **CreateOneOff** pour créer un identificateur d’entrée pour un destinataire unique , un destinataire qui n’appartient à aucun des conteneurs de l’un des fournisseurs de carnets d’adresses actuellement chargés. Les destinataires uniques peuvent avoir n’importe quel type d’adresse pris en charge par l’un des fournisseurs de carnets d’adresses actifs pour la session. 
  
Les destinataires uniques sont généralement créés avec un modèle pour leur type d’adresse particulier. Le fournisseur de carnet d’adresses qui prend en charge le type d’adresse fournit le modèle. Un utilisateur d’une application cliente entre les informations pertinentes dans le modèle.
  
MAPI prend en charge les chaînes de caractères Unicode pour le nom d’affichage, le type d’adresse et les paramètres d’adresse de **CreateOneOff**.
  
L’indicateur MAPI_SEND_NO_RICH_INFO contrôle si le texte mis en forme au format RTF (Rich Text Format) est envoyé avec chaque message. Le format TNEF (Transport Neutral Encapsulation Format), un format utilisé pour la transmission du texte mis en forme, est envoyé par la plupart des fournisseurs de transport, quelle que soit la façon dont le destinataire définit sa propriété **PR_SEND_RICH_INFO** . Il ne s’agit pas d’un problème pour les clients de messagerie qui utilisent des messages interpersonnels. Toutefois, étant donné que TNEF est généralement utilisé pour envoyer des propriétés personnalisées pour les classes de message personnalisées, ne pas le prendre en charge peut être un problème pour les clients basés sur des formulaires ou les clients qui nécessitent des propriétés MAPI personnalisées. Pour plus d’informations, consultez [Envoi de messages avec TNEF](sending-messages-with-tnef.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI utilise la méthode **CreateOneOff** pour créer un ID d’entrée pour une adresse introuvable dans un carnet d’adresses. |
   
## <a name="see-also"></a>Voir aussi



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

