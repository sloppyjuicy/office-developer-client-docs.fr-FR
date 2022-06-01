---
title: IConverterSessionSetSaveFormat
description: IConverterSessionSetSaveFormat définit le format dans lequel le convertisseur retourne un flux MIME dans IConverterSession::MAPIToMIMEStm.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
ms.openlocfilehash: 1aeb3d4f4eab125498857656c152fc27dbc23316
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815757"
---
# <a name="iconvertersessionsetsaveformat"></a>IConverterSession::SetSaveFormat

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit le format dans lequel le convertisseur retourne un flux MIME dans [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a>Paramètres

_mstSaveFormat_
  
> [in] Format d’enregistrement à utiliser pour un flux MIME. Pour plus d’informations, consultez le type d’énumération [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).
    
  - **SAVE_RFC1521** : utilisez MIME, qui est la valeur par défaut.      
  - **SAVE_RFC822** : utilisez uuencode.
    
## <a name="return-values"></a>Valeurs de retour

S_OK
  
> L’appel a réussi.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI. |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML. |
   
## <a name="see-also"></a>Voir aussi

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetEncoding](iconvertersession-setencoding.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [Constantes MAPI](mapi-constants.md)

