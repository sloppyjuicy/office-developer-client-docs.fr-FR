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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432316"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Autorise les conversions entre les objets MIME et les messages MAPI. Cela peut être utile pour transporter des messages sur Internet.
  
|||
|:-----|:-----|
|Fourni par :  <br/> |CLSID_IConverterSession  <br/> |
|Identificateur de l'interface:  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |Spécifie un carnet d'adresses MAPI facultatif que le convertisseur MAPI vers MIME utilise pour résoudre des adresses ambiguës lors de la conversion d'un message MAPI en un flux MIME.  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |Initialise le codage à utiliser pendant la conversion.  <br/> |
| *Membre de l'espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |ConVertit un flux MIME en message MAPI.  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |ConVertit un message MAPI en un flux MIME.  <br/> |
| *Membre de l'espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
| *Membre de l'espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
| *Membre de l'espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |Définit la largeur de l'habillage du texte pour un flux MIME que le convertisseur renvoie dans **MAPIToMIMEStm**.  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |Définit le format que le convertisseur renvoie un flux MIME dans **MAPIToMIMEStm**.  <br/> |
| *Membre de l'espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |Spécifie un jeu de caractères facultatif que le convertisseur MAPI à MIME utilise lors de la conversion d'un message MAPI en un flux MIME.  <br/> |
   
## <a name="remarks"></a>Remarques

Appelez **SetEncoding** avant d'utiliser **MAPIToMIMEStm** pour effectuer la conversion. 
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de conversion MAPI-MIME](about-the-mapi-mime-conversion-api.md)
  
[Constantes MAPI](mapi-constants.md)

