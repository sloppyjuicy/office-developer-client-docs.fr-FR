---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c61b8a1fbcc009eede20bc0dd4827da017774af4
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62789136"
---
# <a name="imslogon--iunknown"></a>IMSLogon : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Accède aux ressources d’un objet d’ouverture de magasin de messages.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposé par :  <br/> |Objets d’ouverture de magasin de messages  <br/> |
|Implémenté par :  <br/> |Fournisseurs de magasins de messages  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMSLogon  <br/> |
|Type de pointeur :  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](imslogon-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur qui s’est produite pour l’objet de la boutique de messages. |
|[Logoff](imslogon-logoff.md) <br/> |Déconnecte un fournisseur de magasins de messages. |
|[OpenEntry](imslogon-openentry.md) <br/> |Ouvre un dossier ou un objet message et renvoie un pointeur vers l’objet pour fournir un accès supplémentaire. |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet. |
|[Conseiller](imslogon-advise.md) <br/> |Enregistre un objet auprès d’un fournisseur de magasins de messages pour les notifications concernant les modifications apportées à la magasin de messages. |
|[Unadvise](imslogon-unadvise.md) <br/> |Supprime l’inscription d’un objet pour la notification des modifications de magasin de messages précédemment établies à l’aide d’un appel à la méthode **IMSLogon::Advise** . |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |Ouvre un objet d’état. |
   
## <a name="remarks"></a>Remarques

L’objet d’ouverture de magasin de messages est la partie d’un fournisseur de magasin de messages ouvert que MAPI appelle directement. Il existe une correspondance un-à-un entre l’objet d’ouverture de conférence de la boutique de messages que MAPI appelle et l’objet de magasin de messages que les applications clientes appellent ; vous pouvez penser à l’ouverture de site et stocker des objets comme un seul objet qui expose deux interfaces. Les deux objets sont créés ensemble et libérés ensemble.
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

