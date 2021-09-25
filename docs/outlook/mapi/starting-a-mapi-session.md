---
title: Démarrage d’une session MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 765bfef3ab30ec4a534f78cc7175394d96d5163c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566380"
---
# <a name="starting-a-mapi-session"></a>Démarrage d’une session MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Bien qu’une quantité importante de travail soit effectuée au démarrage de la session, les tâches requises sont minimes. Une grande partie de ce travail est effectuée dans le traitement MAPI des appels [MAPIInitialize](mapiinitialize.md) et [MAPILogonEx.](mapilogonex.md) Ces deux fonctions acceptent des indicateurs comme paramètres d’entrée pour contrôler des aspects de la session tels que la gestion des notifications et l’interface utilisateur. Il est important de comprendre les conséquences de la définition de chacun de ces indicateurs lors de l’appel de **MAPIInitialize** pour initialiser les bibliothèques MAPI et **MAPILogonEx** pour se connecter au sous-système MAPI. 
  
 **Pour démarrer une session MAPI**
  
1. Appelez **MAPIInitialize** pour initialiser l’ensemble standard de bibliothèques MAPI. 
    
2. Si vous devez utiliser les bibliothèques OLE, appelez la fonction [OLE OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).
    
3. Si vous devez utiliser la bibliothèque d’utilitaires MAPI, appelez [ScInitMapiUtil](scinitmapiutil.md).
    
4. Appelez **MAPILogonEx avec** un profil valide pour vous connecter au sous-système MAPI. **MAPILogonEx** vérifie la configuration de chacun des fournisseurs de services dans les services de messagerie inclus dans le profil, en inviteant l’utilisateur à fournir des informations supplémentaires si nécessaire et possible. Une **fois MAPILogonEx** terminé, les fournisseurs de services configurés sont prêts pour le service. 
    
## <a name="in-this-section"></a>Dans cette section

[Initialisation de MAPI](initializing-mapi.md)
  
> Décrit comment initialiser MAPI pour une session.
    
[Initialisation d’OLE pour MAPI](initializing-ole-for-mapi.md)
  
> Décrit les appels à effectuer pour initialiser OLE à utiliser avec MAPI.
    
[Initialisation des utilitaires MAPI](initializing-the-mapi-utilities.md)
  
> Décrit comment initialiser les utilitaires MAPI.
    
[Connexion à MAPI](logging-on-to-mapi.md)
  
> Décrit comment les applications clientes se connectent au sous-système MAPI.
    

