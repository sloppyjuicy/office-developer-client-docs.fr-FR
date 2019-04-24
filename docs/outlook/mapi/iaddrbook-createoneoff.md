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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 980ac82c6f7fcb5771a6013b3fb033b0bdfd05e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349314"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un identificateur d'entrée pour une adresse ponctuelle.
  
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
  
> dans Pointeur vers la valeur de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du destinataire. Le paramètre _lpszName_ peut être null. 
    
 _lpszAdrType_
  
> dans Pointeur vers le type d'adresse du destinataire, tel que FAX ou SMTP. Le paramètre _lpszAdrType_ ne peut pas être null. 
    
 _lpszAddress_
  
> dans Pointeur vers l'adresse du destinataire. Le paramètre _lpszAddress_ ne peut pas être null. 
    
 _ulFlags_
  
> dans Masque de bits des indicateurs qui affecte le destinataire unique. Les indicateurs suivants peuvent être définis:
    
MAPI_SEND_NO_RICH_INFO 
  
> Le destinataire ne peut pas gérer le contenu du message mis en forme. Si MAPI_SEND_NO_RICH_INFO est défini, MAPI affecte la valeur FALSe à la propriété **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) du destinataire. Si MAPI_SEND_NO_RICH_INFO n'est pas défini, MAPI affecte à cette propriété la valeur TRUE sauf si l'adresse de messagerie du destinataire désignée par _lpszAddress_ est interprétée comme une adresse Internet. Dans ce cas, MAPI définit **PR_SEND_RICH_INFO** sur false. 
    
MAPI_UNICODE 
  
> Le nom complet, le type d'adresse et l'adresse sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, ces chaînes sont au format ANSI.
    
 _lpcbEntryID_
  
> remarquer Pointeur vers le nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lppEntryID_ . 
    
 _lppEntryID_
  
> remarquer Pointeur vers un pointeur vers l'identificateur d'entrée pour le destinataire isolé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'identificateur d'entrée unique a été créé avec succès.
    
## <a name="remarks"></a>Remarques

Les clients appellent la méthode **CreateOneOff** pour créer un identificateur d'entrée pour un destinataire unique, c'est-à-dire un destinataire qui n'appartient à aucun des conteneurs de l'un des fournisseurs de carnets d'adresses actuellement chargés. Les destinataires uniques peuvent avoir n'importe quel type d'adresse pris en charge par l'un des fournisseurs de carnet d'adresses actifs pour la session. 
  
Les destinataires uniques sont généralement créés avec un modèle pour leur type d'adresse particulier. Le fournisseur de carnet d'adresses qui prend en charge le type d'adresse fournit le modèle. Un utilisateur d'une application cliente entre les informations appropriées dans le modèle.
  
MAPI prend en charge les chaînes de caractères Unicode pour le nom complet, le type d'adresse et les paramètres d'adresse de **CreateOneOff**.
  
L'indicateur MAPI_SEND_NO_RICH_INFO contrôle si le texte mis en forme au format RTF (Rich Text Format) est envoyé avec chaque message. Le format TNEF (Transport Neutral Encapsulation Format), qui est utilisé pour transmettre le texte mis en forme, est envoyé par la plupart des fournisseurs de transport, quelle que soit la manière dont le destinataire définit sa propriété **PR_SEND_RICH_INFO** . Ce n'est pas un problème pour les clients de messagerie qui fonctionnent avec des messages interpersonnels. Toutefois, étant donné que le format TNEF est généralement utilisé pour envoyer des propriétés personnalisées pour des classes de message personnalisées, il peut s'agir d'un problème pour les clients de formulaire ou les clients qui nécessitent des propriétés MAPI personnalisées. Pour plus d'informations, consultez la rubrique [envoi de messages avec TNEF](sending-messages-with-tnef.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|Mapiabfunctions. cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI utilise la méthode **CreateOneOff** pour créer un ID d'entrée pour une adresse qui est introuvable dans un carnet d'adresses.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

