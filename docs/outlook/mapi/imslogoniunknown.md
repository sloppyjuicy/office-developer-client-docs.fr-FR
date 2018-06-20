---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 42e2633ac6d534be2c75c47b24c1da5ed9771e18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784302"
---
# <a name="imslogon--iunknown"></a>IMSLogon : IUnknown

  
  
**S’applique à**: Outlook 
  
Ressources d’accès dans un message stockent objet d’ouverture de session.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposés par :  <br/> |Objets de message store d’ouverture de session  <br/> |
|Implémentée par :  <br/> |Fournisseurs de banque de messages  <br/> |
|Appelée par :  <br/> |MAPI  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMSLogon  <br/> |
|Type de pointeur :  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetLastError](imslogon-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur qui s’est produite lors de l’objet de la banque de message.  <br/> |
|[Logoff](imslogon-logoff.md) <br/> |Fournisseur de magasins de journaux d’un message.  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |Ouvre un dossier ou un objet de message et retourne un pointeur vers l’objet pour fournir un accès plus.  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet.  <br/> |
|[Conseiller](imslogon-advise.md) <br/> |Inscrit un objet avec un fournisseur de magasin de message pour les notifications sur les modifications dans la banque de messages.  <br/> |
|[L’avertissement](imslogon-unadvise.md) <br/> |Supprime l’inscription d’un objet pour la notification des modifications de banque de messages précédemment établie à l’aide d’un appel à la méthode **IMSLogon::Advise** .  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |Ouvre un objet d’état.  <br/> |
   
## <a name="remarks"></a>Remarques

L’objet d’ouverture de session du magasin de message est la partie d’un fournisseur de magasins d’ouvrir le message MAPI appelle directement. Il existe une correspondance entre l’objet d’ouverture de session de magasin de message qui stockent des appels MAPI et le message d’objet applications clientes appellent ; Vous pouvez considérer les paramètres de connexion et stocker des objets sous forme d’un objet qui expose les deux interfaces. Les deux objets sont créés, ensemble et libérés ensemble.
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

