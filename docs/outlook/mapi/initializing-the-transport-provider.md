---
title: Initialisation du fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 977c18ce-ece5-4ad1-ac97-5a680846ab83
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 474a8085ca8b82d11efd68c9fd4d8719fe239207
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309680"
---
# <a name="initializing-the-transport-provider"></a>Initialisation du fournisseur de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'interface de spouleur de transport définit les appels que le spouleur MAPI effectue à un fournisseur de transport. Les fournisseurs de transport implémentent ces routines dans une bibliothèque de liens dynamiques (DLL). Le premier point d'entrée direct dans la DLL utilisée par le spouleur MAPI doit être la fonction d'initialisation du fournisseur de transport [XPProviderInit](xpproviderinit.md).
  
MAPI utilise la routine **GetProcAddress** pour obtenir l'adresse de la routine d'initialisation du fournisseur de services, puis appelle cette routine. Le nom de la routine d'initialisation est **XPProviderInit** pour les fournisseurs de transport. Il est différent pour d'autres types de fournisseurs de services MAPI de sorte qu'une DLL puisse contenir n'importe quel ensemble de types de fournisseurs de services, mais un seul fournisseur de services d'un type particulier. Toutefois, un fournisseur de services d'un type donné peut implémenter plusieurs services de son type. Par exemple, un fournisseur de transport peut implémenter la fonctionnalité de transport des messages vers plusieurs services de messagerie. 
  
Le fichier d'en-tête mapispi. h possède une définition de type pour le prototype de fonction de la fonction d'initialisation du fournisseur de transport, ainsi qu'un nom de procédure prédéfini. En nommant les routines d'initialisation dans vos fichiers C et C++ avec les mêmes noms utilisés par **GetProcAddress** et à l'aide d'une déclaration d'exportation simple dans votre dll. DEF, vous obtenez automatiquement le contrôle de type des paramètres de votre routine d'initialisation. Consultez l'exemple de code source de fournisseur de transport pour obtenir des exemples. Pour plus d'informations, consultez la rubrique [exemple de fournisseur de transport](transport-provider-sample.md).
  
Si l'appel de l'initialisation d'un fournisseur de services réussit mais renvoie un numéro de version d'interface du fournisseur de services trop petit pour le traitement MAPI, MAPI appelle immédiatement la méthode **Release** de l'objet fournisseur de services et poursuit comme si l'appel d'initialisation échec avec MAPI_E_VERSION. De cette façon, MAPI et le fournisseur de services définissent conjointement la plage de numéros de version de l'interface du fournisseur de services qu'ils peuvent gérer, et si rien ne correspond, le chargement du fournisseur de services échoue avec une valeur de retour MAPI_E_VERSION. 
  
La dernière étape pour le spouleur MAPI lors de l'accès aux ressources du fournisseur de services consiste à ouvrir une session sur le fournisseur de transport. Le spouleur MAPI appelle la méthode [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) de l'objet [IXPProvider: IUnknown](ixpprovideriunknown.md) renvoyé à partir de **XPProviderInit**. Il s'agit de l'appel dans lequel les informations d'identification, le cas échéant, sont vérifiées et les boîtes de dialogue peuvent être autorisées.
  
Si un processus ouvre une deuxième session de transport sur le même fournisseur de transport et la même session MAPI, la DLL du fournisseur de transport ne doit pas créer de deuxième objet fournisseur. Le premier objet Provider doit être utilisé pour se connecter à la deuxième session de transport. Un fournisseur de transport doit être programmé pour prendre en charge plusieurs sessions de transport dans un seul objet fournisseur. Un deuxième objet Provider ne doit être créé que si différentes sessions MAPI sont utilisées dans le même processus.
  

