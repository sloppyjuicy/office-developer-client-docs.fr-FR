---
title: IConverterSessionSetAdrBook
description: IConverterSessionSetAdrBook spécifie un carnet d’adresses MAPI facultatif que le convertisseur MAPI en MIME utilise pour résoudre les adresses ambiguës.
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
ms.openlocfilehash: 92af9737bf3d65f696b02c091f8401fc7f27a669
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815771"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie un carnet d’adresses MAPI facultatif que le convertisseur MAPI en MIME utilise pour résoudre les adresses ambiguës lors de la conversion d’un message MAPI en flux MIME.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Paramètres

 _Pab_
  
> [in] Pointeur vers une interface [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) à utiliser dans la conversion MAPI en MIME. Définissez ce paramètre sur **Null** lorsque vous n’avez plus besoin du carnet d’adresses ; cela libère l’interface et réinitialise le convertisseur pour qu’il n’utilise pas de carnet d’adresses. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’appel de fonction réussit.
    
## <a name="remarks"></a>Remarques

La conversion d’un message MAPI en flux MIME ne nécessite généralement pas de connexion à un profil MAPI. Toutefois, la spécification d’un carnet d’adresses MAPI pour la conversion nécessite une connexion à un profil pour obtenir le carnet d’adresses.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI. |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML. |
   
## <a name="see-also"></a>Voir aussi



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

