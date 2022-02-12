---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: 'Last modified: September 20, 2017'
ms.openlocfilehash: 1b0ef4f6a314119235e57fbf41b3577e4cf334de
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62779986"
---
# <a name="iconvertersessionmapitomimestm"></a>IConverterSession::MAPIToMIMEStm
 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Convertit un message MAPI en flux MIME.
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Paramètres

 _pmsg_
  
> [in] Pointeur vers le message à convertir. Voir mapidefs.h pour la définition de type **de LPMESSAGE**.
    
 _pstm_
  
> [out] [Interface IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) pour la sortie du flux. 
    
 _ulFlags_
  
>  [in] Indicateurs qui indiquent des actions spécifiques pour le convertisseur : 
    
CCSF_8BITHEADERS
  
> Le convertisseur doit autoriser les en-têtes 8 bits.
    
CCSF_EMBEDDED_MESSAGE
  
> Les informations envoyées/non envoyées sont persistantes dans X-Unsent.
    
CCSF_GLOBAL_MESSAGE
  
> Le convertisseur doit créer un message international (EAI/RFC6530).
    
CCSF_INCLUDE_BCC
  
> Les destinataires Bc du message MAPI doivent être inclus dans le flux MIME.
    
CCSF_NO_MSGID
  
> N’incluez pas Message-Id champ dans les messages sortants.
    
CCSF_NOHEADERS
  
> Le convertisseur doit ignorer les en-têtes du message externe.
    
CCSF_PLAIN_TEXT_ONLY
  
> Le convertisseur doit simplement envoyer du texte simple.
    
CCSF_SMTP
  
> Un message SMTP est transmis au convertisseur. Cet indicateur doit toujours être définie.
    
CCSF_USE_RTF
  
> Le convertisseur doit convertir du format HTML au format RTF dans le message MIME.
    
CCSF_USE_TNEF
  
> Le convertisseur doit utiliser le format TNEF (Transport Neutral Encapsulation Format) dans le message MIME.
    
## <a name="return-values"></a>Valeurs de retour

E_INVALIDARG
  
> Des indicateurs non valides ont été passés ou  *pmsg*  ou  *pstm*  a la valeur NULL. 
    
## <a name="remarks"></a>Remarques

Pris en charge uniquement pour les types de messages Outlook standard.
  
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
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
  
[Propriété canonique PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)
  
[Propri�t� canonique PidLidUseTnef](pidlidusetnef-canonical-property.md)


[Constantes MAPI](mapi-constants.md)

