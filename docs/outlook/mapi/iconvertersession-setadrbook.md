---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ae00fd0711b8fcae01db6a89da7607d79d8757c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584358"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Spécifie une option carnet d’adresses MAPI par l’interface MAPI convertisseur MIME pour résoudre les adresses ambigus lors de la conversion d’un message MAPI à un flux de données MIME.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Paramètres

 _Carnet d’adresses personnel_
  
> [in] Pointeur vers une [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface à utiliser dans la conversion MAPI MIME. Définissez ce paramètre sur **null** lorsque vous n’avez plus besoin du carnet d’adresses ; Cela libère l’interface et réinitialise le convertisseur ne pas à l’aide de n’importe quel carnet d’adresses. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> L’appel de fonction a réussi.
    
## <a name="remarks"></a>Remarques

Conversion d’une MAPI message MIME stream généralement ne nécessite pas se connecter à un profil MAPI. Toutefois, la spécification d’un carnet d’adresses de MAPI pour la conversion de requiert ouvrent une session sur un profil pour obtenir le carnet d’adresses.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI utilise MimeToMAPI pour convertir un fichier EML à un message MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI utilise MAPIToMIMEStm pour convertir un message MAPI dans un fichier EML.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

