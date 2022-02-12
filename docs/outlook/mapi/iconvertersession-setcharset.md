---
title: IConverterSessionSetCharSet
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
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 441d9915ee0e3f5832125dfd6677a0f7b0823b74
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772160"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie un jeu de caractères facultatif que le convertisseur MAPI en MIME utilise lors de la conversion d’un message MAPI en flux MIME.
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Paramètres

 _fApply_
  
> [in] Indique s’il faut utiliser un jeu de caractères spécifique pour la conversion. Définissez ce paramètre sur **true** pour appliquer le jeu de caractères dans les conversions suivantes. Définissez ce paramètre sur **false** si vous ne souhaitez plus appliquer de jeu de caractères spécifique et revenir aux valeurs par défaut pour les messages suivants. 
    
 _hcharset_
  
> [in] Handle vers un jeu de caractères défini dans mimeole.h de Windows Mail. **Spécifiez null** pour spécifier que vous ne souhaitez pas appliquer de jeu de caractères spécifique. Pour les valeurs **non null** , utilisez une fonction telle que [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) pour obtenir un handle pour le jeu de caractères. 
    
 _csetapplytype_
  
> [in] Indique comment appliquer un jeu de caractères pour convertir un message, tel que défini dans mimeole.h de Windows Mail.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’appel de fonction a réussi.
    
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
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

