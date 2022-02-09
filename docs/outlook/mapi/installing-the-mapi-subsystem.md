---
title: Installation du sous-système MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: Dernière modification le 9 mars 2015
ms.localizationpriority: high
ms.openlocfilehash: 65e967a2414257fceb856668f99d97a0819b92b1
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462339"
---
# <a name="installing-the-mapi-subsystem"></a>Installation du sous-système MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les versions prises en charge de Windows installent la bibliothèque stub MAPI, Mapi32.dll, dans le dossier _\<drive\>_ \Windows\System32. 
  
Voici les versions prises en charge de Windows :
  
- Windows 7
    
- Windows Vista
    
- Windows Server 2008
    
- Windows Server 2003
    
- Windows XP
    
Pour installer correctement le sous-système MAPI, installez une application qui contient un sous-système de MAPI, tel que Microsoft Outlook.
  
Vous trouverez des informations sur l’installation du sous-système MAPI d’un ordinateur dans le Registre système. Toutes les valeurs indiquées dans les entrées du registre sont des chaînes de caractères. 
  
Les programmes d’installation de service de messagerie sont chargés de créer les informations d’installation dans la clé du Registre système suivante : 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
Les services de messagerie doivent ajouter des entrées au Registre système. 
  
Le tableau suivant récapitule comment les clients récupèrent les informations de version pour le sous-système MAPI sur leur ordinateur.
  
|**Pour vérifier**|**Registre**|
|:-----|:-----|
|Disponibilité de MAPI  <br/> |Rechercher `MAPIX=1`.  <br/> |
|Version disponible de MAPI  <br/> |Rechercher une chaîne MAPIXVER au format « _x.x.x_ ».  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la programmation MAPI](mapi-programming-overview.md)

