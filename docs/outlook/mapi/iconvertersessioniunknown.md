---
title: IConverterSession IUnknown
description: IConverterSession IUnknown autorise les conversions entre les objets MIME et les messages MAPI, ce qui peut être utile pour le transport de messages sur Internet.
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
ms.openlocfilehash: 69be502dea3b6cb4482e2eafe01ecdc7ce37ce1f
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65818200"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Autorise les conversions entre les objets MIME et les messages MAPI. Cela peut être utile pour le transport de messages sur Internet.
  
|Propriété |Valeur |
|:-----|:-----|
|Fourni par :  <br/> |CLSID_IConverterSession  <br/> |
|Identificateur d’interface :  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Membre |Valeur |
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |Spécifie un carnet d’adresses MAPI facultatif que le convertisseur MAPI en MIME utilise pour résoudre les adresses ambiguës lors de la conversion d’un message MAPI en flux MIME. |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |Initialise l’encodage à utiliser pendant la conversion. |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |Convertit un flux MIME en message MAPI. |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |Convertit un message MAPI en flux MIME. |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |Définit la largeur d’habillage du texte pour un flux MIME retourné par le convertisseur dans **MAPIToMIMEStm**. |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |Définit le format auquel le convertisseur retourne un flux MIME dans **MAPIToMIMEStm**. |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |Spécifie un jeu de caractères facultatif que le convertisseur MAPI en MIME utilise lors de la conversion d’un message MAPI en flux MIME. |
   
## <a name="remarks"></a>Remarques

Appelez **SetEncoding** avant d’utiliser **MAPIToMIMEStm** pour effectuer la conversion. 
  
## <a name="see-also"></a>Voir aussi



[À propos de l’API de conversion MAPI-MIME](about-the-mapi-mime-conversion-api.md)
  
[Constantes MAPI](mapi-constants.md)

