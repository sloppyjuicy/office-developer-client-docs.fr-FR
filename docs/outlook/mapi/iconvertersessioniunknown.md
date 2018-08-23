---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 316e17e7804e754eed4ee4fef27211fb5173d4bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589643"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Permet les conversions entre objets MIME et les messages MAPI. Cela peut être utile de transport des messages via Internet.
  
|||
|:-----|:-----|
|Fourni par :  <br/> |CLSID_IConverterSession  <br/> |
|Identificateur de l’interface :  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |Spécifie une option carnet d’adresses MAPI par l’interface MAPI convertisseur MIME pour résoudre les adresses ambigus lors de la conversion d’un message MAPI à un flux de données MIME.  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |Initialise le codage à utiliser lors de la conversion.  <br/> |
| *Membres de l’espace réservé*  <br/> | *Non pris en charge ou documentés.*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |Convertit un flux de données MIME à un message MAPI.  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |Convertit un message MAPI à un flux de données MIME.  <br/> |
| *Membres de l’espace réservé*  <br/> | *Non pris en charge ou documentés.*  <br/> |
| *Membres de l’espace réservé*  <br/> | *Non pris en charge ou documentés.*  <br/> |
| *Membres de l’espace réservé*  <br/> | *Non pris en charge ou documentés.*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |Définit la largeur d’un flux MIME qui retourne le convertisseur **MAPIToMIMEStm**d’habillage de texte.  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |Définit le format que le convertisseur retourne un flux de données MIME dans **MAPIToMIMEStm**.  <br/> |
| *Membres de l’espace réservé*  <br/> | *Non pris en charge ou documentés.*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |Spécifie un caractère facultatif que l’interface MAPI convertisseur MIME utilise lors de la conversion d’un message MAPI à un flux de données MIME.  <br/> |
   
## <a name="remarks"></a>Remarques

Appelez **SetEncoding** avant d’utiliser **MAPIToMIMEStm** pour effectuer la conversion. 
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de conversion MAPI-MIME](about-the-mapi-mime-conversion-api.md)
  
[Constantes MAPI](mapi-constants.md)

