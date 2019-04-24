---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7645208e6a0256957deb3a71ba3e04ad125a6b61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326893"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie un carnet d'adresses MAPI facultatif que le convertisseur MAPI vers MIME utilise pour résoudre des adresses ambiguës lors de la conversion d'un message MAPI en un flux MIME.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Paramètres

 _Cap_
  
> dans Pointeur vers une interface [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) à utiliser dans la conversion MAPI vers MIME. Définissez ce paramètre sur **null** lorsque vous n'avez plus besoin du carnet d'adresses; Cela libère l'interface et réinitialise le convertisseur de sorte qu'il n'utilise aucun carnet d'adresses. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel de fonction est réussi.
    
## <a name="remarks"></a>Remarques

La conversion d'un message MAPI en flux MIME n'exige généralement pas l'ouverture d'une session sur un profil MAPI. Toutefois, si vous spécifiez un carnet d'adresses MAPI pour la conversion, vous devez vous connecter à un profil pour obtenir le carnet d'adresses.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MapiMime. cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI.  <br/> |
|MapiMime. cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

