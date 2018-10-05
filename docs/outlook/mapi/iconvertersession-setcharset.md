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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 14b2904e57852c564395f4b27c9d5270afd1454a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385724"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie qu'un caractère facultatif configurer que l’interface MAPI à MIME convertisseur utiliser lors de la conversion d’un message MAPI à un flux de données MIME.
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Paramètres

 _fApply_
  
> [in] Indique s’il faut utiliser un caractère spécifique défini pour la conversion. Définissez ce paramètre sur **true** pour appliquer le jeu de caractères dans les conversions suivantes. Définissez ce paramètre sur **false** si vous ne souhaitez plus appliquer n’importe quel jeu de caractères spécifique et revenir à la valeur par défaut pour les messages suivants. 
    
 _hcharset_
  
> [in] Handle vers un jeu défini dans mimeole.h de Windows Mail de caractères. Spécifiez **null** pour spécifier que vous ne souhaitez pas appliquer n’importe quel jeu de caractères spécifique. Pour des valeurs non - **null** , utilisez la fonction telles que [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) pour obtenir un handle vers le jeu de caractères. 
    
 _csetapplytype_
  
> [in] Indique comment appliquer un jeu de caractères à convertir un message, comme défini dans mimeole.h de Windows Mail.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’appel de fonction a réussi.
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utilise MimeToMAPI pour convertir un fichier EML à un message MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI dans un fichier EML.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

