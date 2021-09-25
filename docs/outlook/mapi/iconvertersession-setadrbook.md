---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d05b08cd18b075119017163c7142e88afba82121
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600983"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie un carnet d’adresses MAPI facultatif que le convertisseur MAPI en MIME utilise pour résoudre des adresses ambiguës lors de la conversion d’un message MAPI en flux MIME.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Paramètres

 _pab_
  
> [in] Pointeur vers une interface [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) à utiliser dans la conversion MAPI vers MIME. Définissez ce paramètre sur **null** lorsque vous n’avez plus besoin du carnet d’adresses ; Cela libère l’interface et réinitialise le convertisseur pour qu’il n’utilise aucun carnet d’adresses. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’appel de fonction a réussi.
    
## <a name="remarks"></a>Remarques

En règle générale, la conversion d’un message MAPI en flux MIME ne nécessite pas de connexion à un profil MAPI. Toutefois, la spécification d’un carnet d’adresses MAPI pour la conversion nécessite une connexion à un profil pour obtenir le carnet d’adresses.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

