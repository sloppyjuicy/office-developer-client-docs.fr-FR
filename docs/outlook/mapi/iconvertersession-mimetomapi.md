---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 60a058cc119290a0e14a76c914ac6d5a2d7a693b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593017"
---
# <a name="iconvertersessionmimetomapi"></a>IConverterSession::MIMEToMAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Convertit un flux de données MIME à un message MAPI.
  
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
  
> [in] Interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) pour un flux de données MIME. 
    
 _pMsg_
  
> [out] Pointeur vers le message à charger. Voir mapidefs.h pour la définition du type de **LPMESSAGE**.
    
 _pszSrcSrv_
  
> [in] Cette valeur doit être **null**.
    
 _ulFlags_
  
> [in] Ce paramètre identifie l’action particulière à prendre lors de la conversion. Il doit être égal à zéro (0) si aucune action n’est prise en ou une combinaison des valeurs suivantes :
    
CCSF_EMBEDDED_MESSAGE
  
> Informations envoyées/en attente ne sont conservées dans X-en attente.
    
CCSF_SMTP
  
> Le flux MIME est un message Simple MAPI Transfer Protocol (SMTP).
    
CCSF_INCLUDE_BCC
  
> Les destinataires Cci du flux MIME doivent être inclus dans le message MAPI.
    
CCSF_USE_RTF
  
> Le corps HTML de l’objet stream MIME doivent être converti au Format RTF (RICH Text Format) dans le message MAPI.
    
## <a name="return-value"></a>Valeur renvoy�e

E_INVALIDARG
  
> Indique que _pstm_ a la **valeur null**, _pmsg_ est **null**ou _ulFlags_ n’est pas valide. 
    
## <a name="remarks"></a>Remarques

Si vous avez spécifié **CCSF_USE_RTF** dans le cadre de _ulFlags_ et la banque de messages de destination prend en charge HTML et RTF, le message MAPI est converti au format HTML ou RTF. Si le message est converti au format RTF, au format converti est compressé au format RTF, HTML sera incorporée dans la chaîne de format RTF compressée, et la chaîne figure dans la [Propriété canonique PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utilise MimeToMAPI pour convertir un fichier EML à un message MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI dans un fichier EML.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[Constantes MAPI](mapi-constants.md)

