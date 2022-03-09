---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Last modified: September 06, 2019'
ms.openlocfilehash: 8d6b393fd957ef14cb86bcd26e343716e852a84a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382383"
---
# <a name="iconvertersessionmimetomapi"></a>IConverterSession::MIMEToMAPI

**S’applique à** : Outlook 2013 | Outlook 2016

Convertit un flux MIME en message MAPI.

```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a>Paramètres

 _pstm_

> [in] [Interface IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) vers un flux MIME.

 _pmsg_

> [in] Pointeur vers le message à charger. L’appelant doit fournir un message à remplir par l’API, de sorte que l’objet doit y aller. Voir mapidefs.h pour la définition de type **de LPMESSAGE**.

 _pszSrcSrv_

> [in] Cette valeur doit être **null**.

 _ulFlags_

> [in] Ce paramètre identifie toute action spéciale à prendre pendant la conversion. Elle doit être zéro (0) si aucune action spécifique n’est à prendre, ou une combinaison des valeurs suivantes :

CCSF_EMBEDDED_MESSAGE

> Les informations envoyées/non envoyées sont persistantes dans X-Unsent.

CCSF_SMTP

> Le flux MIME est pour un message SMTP (Simple Mail Transfer Protocol).

CCSF_INCLUDE_BCC

> Les destinataires  BcC du flux MIME doivent être inclus dans le message MAPI.

CCSF_USE_RTF

> Le corps HTML du flux MIME doit être converti au format RTF (Rich Text Format) dans le message MAPI.

CCSF_GLOBAL_MESSAGE
> Le convertisseur doit gérer le flux MIME en tant que message international (EAI/RFC6530). Non pris en charge Outlook 2013.

## <a name="return-value"></a>Valeur renvoyée

E_INVALIDARG

> Indique que _pstm est_ **null**, _pmsg est_ **null** ou _ulFlags_ n’est pas valide.

## <a name="remarks"></a>Remarques

Si vous avez spécifié **CCSF_USE_RTF** dans le cadre de _ulFlags_ et que la boutique de messages de destination prend en charge html et RTF, le message MAPI est converti au format HTML ou RTF. Si le message est converti au format RTF, le format converti sera compressé RTF, tout html sera incorporé dans la chaîne RTF compressée et la chaîne sera contenue dans la propriété canonique [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).

## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.

|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI. |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML. |

## <a name="see-also"></a>Voir aussi

[IConverterSession : IUnknown](iconvertersessioniunknown.md)  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
 [Constantes MAPI](mapi-constants.md)
