---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Dernière modification : 05 juillet 2012'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391947"
---
# <a name="dntble"></a>DNTBLE

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informations relatives au téléchargement du contenu d’un dossier à partir du serveur pendant le [téléchargement de l’état de la table](download-table-state.md). Ce processus de téléchargement utilise une méthode de synchronisation des modifications incrémentielle (ICS) de Microsoft Exchange. Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
## <a name="quick-info"></a>Informations rapides

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a>Membres

 _cEntNew_
  
> [sortant] Nombre d’éléments ajoutés à la banque locale. Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.
    
 _cEntMod_
  
> [sortant] Nombre d’éléments modifiés dans la banque locale. Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.
    
 _cEntRead_
  
> [sortant] Nombre d’éléments lus ou marqués comme non lus dans la banque locale. Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.
    
 _cEntDel_
  
> [sortant] Nombre d’éléments supprimés de la banque locale. Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.
    
## <a name="see-also"></a>Voir aussi



[À propos de la machine à états de réplication](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[DNTBL](dntbl.md)

