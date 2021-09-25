---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 99415e9b3996ead409df7bd99379d39e9a62370e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567626"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Autorise les conversions entre les objets MIME et les messages MAPI. Cela peut être utile pour le transport de messages sur Internet.
  
|||
|:-----|:-----|
|Fourni par :  <br/> |CLSID_IConverterSession  <br/> |
|Identificateur d’interface :  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |Spécifie un carnet d’adresses MAPI facultatif que le convertisseur MAPI en MIME utilise pour résoudre des adresses ambiguës lors de la conversion d’un message MAPI en flux MIME.  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |Initialise le codage à utiliser lors de la conversion.  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |Convertit un flux MIME en message MAPI.  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |Convertit un message MAPI en flux MIME.  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |Définit la largeur du retour à la ligne de texte pour un flux MIME que le convertisseur renvoie dans **MAPIToMIMEStm**.  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |Définit le format que le convertisseur renvoie un flux MIME dans **MAPIToMIMEStm**.  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |Spécifie un jeu de caractères facultatif que le convertisseur MAPI en MIME utilise lors de la conversion d’un message MAPI en flux MIME.  <br/> |
   
## <a name="remarks"></a>Remarques

Appelez **SetEncoding avant** d’utiliser **MAPIToMIMEStm** pour effectuer la conversion. 
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de conversion MAPI-MIME](about-the-mapi-mime-conversion-api.md)
  
[Constantes MAPI](mapi-constants.md)

