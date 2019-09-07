---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Dernière modification : septembre 06, 2019'
ms.openlocfilehash: f6f671cbfd5e14d602aaa31d31e54e859f068593
ms.sourcegitcommit: 27a9f3568318470e7ee09ad93a90c3f80d3ef0cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2019
ms.locfileid: "36790770"
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
  
> dans Interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) à un flux MIME. 
    
 _pmsg_
  
> dans Pointeur vers le message à charger. L’appelant doit fournir un message pour que l’API le remplisse, afin que l’objet soit placé [in]. Voir mapidefs. h pour la définition de type de **LPMESSAGE**.
    
 _pszSrcSrv_
  
> dans Cette valeur doit être **null**.
    
 _ulFlags_
  
> dans Ce paramètre identifie toute action spéciale à effectuer lors de la conversion. Elle doit être égale à zéro (0) si aucune action spécifique n’est effectuée, ou une combinaison des valeurs suivantes :
    
CCSF_EMBEDDED_MESSAGE
  
> Les informations envoyées/non envoyées sont conservées dans X-non envoyés.
    
CCSF_SMTP
  
> Le flux MIME est destiné à un message SMTP (simple MAPI Transfer Protocol).
    
CCSF_INCLUDE_BCC
  
> Les destinataires en copie carbone invisible du flux MIME doivent être inclus dans le message MAPI.
    
CCSF_USE_RTF
  
> Le corps HTML du flux MIME doit être converti au format RTF (Rich Text Format) dans le message MAPI.

CCSF_GLOBAL_MESSAGE
> Le convertisseur doit gérer le flux MIME en tant que message international (EAI/RFC6530). Non pris en charge sur Outlook 2013.
    
## <a name="return-value"></a>Valeur renvoyée

E_INVALIDARG
  
> Indique que _pstm_ est **null**, _PMSG_ est **null**ou _ulFlags_ n’est pas valide. 
    
## <a name="remarks"></a>Remarques

Si vous avez spécifié **CCSF_USE_RTF** dans le cadre de _ulFlags_ et que la Banque de messages de destination prend en charge à la fois le format HTML et le format RTF, le message MAPI est converti au format HTML ou RTF. Si le message est converti au format RTF, le format converti sera au format RTF compressé, tous les éléments HTML seront incorporés dans la chaîne RTF compressée, et la chaîne sera contenue dans la [propriété canonique PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MapiMime. cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utilise MimeToMAPI pour convertir un fichier EML en message MAPI.  <br/> |
|MapiMime. cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI en fichier EML.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[Constantes MAPI](mapi-constants.md)

