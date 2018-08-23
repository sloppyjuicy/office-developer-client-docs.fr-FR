---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ddb87af4b14be6d728bcceddb4d958ba49229ad4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579038"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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

 _Caractère_
  
> [in] Pointeur vers la valeur de la propriété du destinataire **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Le paramètre _le caractère_ peut être NULL. 
    
 _lpszAdrType_
  
> [in] Pointeur vers le type d’adresse du destinataire, tel que FAX ou SMTP. Le paramètre _lpszAdrType_ ne peut pas être NULL. 
    
 _lpszAddress_
  
> [in] Pointeur vers l’adresse du destinataire. Le paramètre _lpszAddress_ ne peut pas être NULL. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs influençant le destinataire unique. Les indicateurs suivants peuvent être définis :
    
MAPI_SEND_NO_RICH_INFO 
  
> Le destinataire ne peut pas gérer le contenu des messages mis en forme. Si MAPI_SEND_NO_RICH_INFO est défini, MAPI définit la propriété du destinataire **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) sur FALSE. Si MAPI_SEND_NO_RICH_INFO n’est pas définie, MAPI définit cette propriété sur TRUE, sauf si l’adresse de messagerie du destinataire désigné par _lpszAddress_ est interprétée comme une adresse Internet. Dans ce cas, MAPI définit **PR_SEND_RICH_INFO** sur FALSE. 
    
MAPI_UNICODE 
  
> Le nom complet, le type d’adresse et l’adresse sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, ces chaînes sont au format ANSI.
    
 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée pour le destinataire unique.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’identificateur d’entrée unique a été créé avec succès.
    
## <a name="remarks"></a>Remarques

Les clients appeler la méthode **CreateOneOff** pour créer un identificateur d’entrée pour un destinataire unique, un destinataire qui n’appartient pas à tous les conteneurs à partir des fournisseurs de carnet d’adresses actuellement chargée. Destinataires uniques peuvent avoir n’importe quel type d’adresse est prise en charge par un des fournisseurs de carnet d’adresses actif pour la session. 
  
Destinataires uniques sont généralement créés avec un modèle pour leur type d’adresse spécifique. Le fournisseur de carnet d’adresses qui prend en charge le type d’adresse fournit le modèle. Un utilisateur d’une application cliente entre les informations appropriées dans le modèle.
  
MAPI prend en charge les chaînes de caractères Unicode pour le nom complet, type d’adresse et les paramètres d’adresse de **CreateOneOff**.
  
L’indicateur MAPI_SEND_NO_RICH_INFO contrôle si le texte mis en forme au format RTF (RICH Text Format) est envoyé avec chaque message. Le Neutral Encapsulation Format TNEF (Transport) : un format qui est utilisé pour la transmission de texte mis en forme — envoyée par la plupart des fournisseurs de transport, quelle que soit la façon dont le destinataire définit sa propriété **PR_SEND_RICH_INFO** . Il n’est pas un problème pour les clients qui fonctionnent avec les messages interpersonnels de messagerie. Toutefois, étant donné que TNEF est généralement utilisé pour envoyer des propriétés personnalisées pour les classes de message personnalisées, non prise en charge peut être un problème pour les clients basés sur les formulaires ou les clients qui requièrent des propriétés MAPI personnalisées. Pour plus d’informations, consultez [Envoi de Messages avec TNEF](sending-messages-with-tnef.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI utilise la méthode **CreateOneOff** pour créer un ID d’entrée pour une adresse qui ne figure pas dans un carnet d’adresses.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

