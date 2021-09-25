---
title: IConverterSessionSetEncoding
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
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7d1862f7aeae4c4bf2d1f6d1fb249a4ce90e18e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613932"
---
# <a name="iconvertersessionsetencoding"></a>IConverterSession::SetEncoding

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Initialise le codage à utiliser lors de la conversion.
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a>Paramètres

_et_
  
> Valeur [ENCODINGTYPE.](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) Seules les valeurs suivantes sont pris en charge : 
    
   - IET_BASE64
   - IET_UUENCODE
   - IET_QP
   - IET_7BIT
   - IET_8BIT
    
## <a name="return-value"></a>Valeur renvoyée

E_INVALIDARG
  
> Le type d’encodage transmis n’était pas valide.
    
## <a name="remarks"></a>Remarques

Appelez **SetEncoding** avant d’utiliser [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) pour effectuer la conversion. 
  
Utilisez **SetEncoding pour** définir le codage uniquement pour le corps de message le plus à l’extérieur d’un élément de courrier. Microsoft Outlook 2010 et Microsoft Outlook 2013 choisir le codage des pièces jointes individuelles. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [Constantes MAPI](mapi-constants.md)

