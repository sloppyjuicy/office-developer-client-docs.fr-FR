---
title: IConverterSessionSetCharSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 14b2904e57852c564395f4b27c9d5270afd1454a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336658"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie un jeu de caractères facultatif que le convertisseur MAPI à MIME utilise lors de la conversion d'un message MAPI en un flux MIME.
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Paramètres

 _fApply_
  
> dans Indique s'il faut utiliser un jeu de caractères spécifique pour la conversion. Définissez ce paramètre sur **true** pour appliquer le jeu de caractères dans les conversions suivantes. Définissez ce paramètre sur **false** si vous ne souhaitez plus appliquer un jeu de caractères spécifique et revenir aux valeurs par défaut pour les messages suivants. 
    
 _hcharset_
  
> dans Un handle vers un jeu de caractères tel qu'il est défini dans MimeOLE. h de Windows Mail. Spécifiez **null** pour spécifier que vous ne souhaitez pas appliquer un jeu de caractères spécifique. Pour les valeurs **** non nulles, utilisez une fonction telle que [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) pour obtenir un descripteur du jeu de caractères. 
    
 _csetapplytype_
  
> dans Indique comment appliquer un jeu de caractères pour convertir un message, tel qu'il est défini dans MimeOLE. h de Windows Mail.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L'appel de fonction est réussi.
    
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
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

