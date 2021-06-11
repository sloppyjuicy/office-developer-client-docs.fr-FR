---
title: Automatisation d’InfoPath à partir d’une application externe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath fournit l’automatisation de l’application à partir du code écrit à l’aide de COM et d’un script à l’aide des méthodes de l’objet Application et de la collection XDocuments.
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412666"
---
# <a name="automating-infopath-from-an-external-application"></a>Automatisation d’InfoPath à partir d’une application externe

Microsoft InfoPath fournit l’automatisation de l’application à partir du code écrit à l’aide de COM et d’un script à l’aide des méthodes de l’objet **Application** et de la collection **XDocuments.** 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a>Vue d’ensemble des objets Application et XDocument

**L’objet Application** contient les méthodes suivantes utilisées pour l’automatisation : 
  
|**Méthode**|**Description**|
|:-----|:-----|
|**CacheSolution** <br/> |Examine le contenu du cache et, si nécessaire, le met à jour à partir de l’emplacement publié du modèle de formulaire.  <br/> |
|**Quit** <br/> |Quitte l’Microsoft Office’application InfoPath.  <br/> |
|**RegisterSolution** <br/> |Installe le modèle de formulaire InfoPath Microsoft Office spécifié.  <br/> |
|**UnregisterSolution** <br/> |Désinstalle le modèle de formulaire InfoPath Microsoft Office spécifié.  <br/> |
   
La collection **XDocuments** contient les méthodes suivantes qui peuvent être utilisées pour l’automatisation externe : 
  
|**Méthode**|**Description**|
|:-----|:-----|
|Méthode **Close**  <br/> |Ferme le formulaire InfoPath Microsoft Office spécifié.  <br/> |
|**Nouvelle** méthode  <br/> |Crée une nouvelle Microsoft Office formulaire InfoPath.  <br/> |
|**Méthode NewFromSolution**  <br/> |Crée un nouveau Microsoft Office Formulaire InfoPath basé sur le modèle de formulaire spécifié.  <br/> |
|**Méthode NewFromSolutionWithData**  <br/> |Crée une nouvelle Microsoft Office formulaire InfoPath à l’aide des données XML et du modèle de formulaire spécifiés.  <br/> |
|**Méthode Open**  <br/> |Ouvre le formulaire InfoPath Microsoft Office spécifié.  <br/> |
   
Pour utiliser l’objet **Application** à partir d’une application externe, utilisez la fonction **CreateObject** avec le ProgID de l’application InfoPath (« InfoPath.Application ») pour créer une variable objet qui représente l’application InfoPath. Vous pouvez ensuite utiliser la **propriété XDocuments** pour accéder à la collection **XDocuments** et utiliser ses méthodes pour ouvrir ou créer un formulaire InfoPath. L’exemple suivant illustre la création d’une référence à l’objet **Application** à l’aide du langage de programmation Microsoft Visual Basic 6.0 ou Visual Basic pour Applications (VBA) : 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> Étant donné que **la fonction CreateObject** crée une variable objet à l’aide de la liaison tardive, l’achèvement automatique des instructions ne sera pas disponible dans l’éditeur Visual Basic. Reportez-vous aux liens des tableaux précédents pour plus d’informations sur la syntaxe d’appel correcte. 
  

