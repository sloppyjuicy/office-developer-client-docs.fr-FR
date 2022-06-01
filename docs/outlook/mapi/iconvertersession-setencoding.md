---
title: IConverterSessionSetEncoding
description: IConverterSessionSetEncoding initialise l’encodage à utiliser pendant la conversion. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
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
ms.openlocfilehash: 15337b8364d2bb1824ee5a35f415ce34945421f7
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816198"
---
# <a name="iconvertersessionsetencoding"></a>IConverterSession::SetEncoding

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Initialise l’encodage à utiliser lors de la conversion.
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a>Paramètres

_et_
  
> Valeur [ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) . Seules les valeurs suivantes sont prises en charge : 
    
   - IET_BASE64
   - IET_UUENCODE
   - IET_QP
   - IET_7BIT
   - IET_8BIT
    
## <a name="return-value"></a>Valeur renvoyée

E_INVALIDARG
  
> Le type d’encodage passé n’était pas valide.
    
## <a name="remarks"></a>Remarques

Appelez **SetEncoding** avant d’utiliser [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) pour effectuer la conversion. 
  
Utilisez **SetEncoding** pour définir l’encodage uniquement pour le corps de message le plus à l’extérieur d’un élément de messagerie. Microsoft Outlook 2010 et Microsoft Outlook 2013 choisissez l’encodage des pièces jointes individuelles. 
  
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
- [IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [Constantes MAPI](mapi-constants.md)

