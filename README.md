# Notice_Api

It allows you to perform CRUD operations (Create, Read, Update, Delete) on notices with ease.

## Features

- Create new notices.
- Retrieve details of existing notices.
- Update information for a specific notice.
- Delete a notice from the system.

## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`PORT` = 3000

`DATABASE_URL` = "postgresql://nameofPostgrsql:password@localhost:5432/nameofDB?schema=public"


## Installation

Install my-project with npm

```bash
  npm install 

```
    
## Deployment



Start the project 

```bash
  npm run dev
```


## API Reference

#### GET all notice

```http
 api/notice
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `api_key` | `string` | **Required**. Your API key |

#### Get notice by id

```http
 api/notice/:id
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `id`      | `string` | **Required**. Id of notice to fetch |

#### GET notice by search

```http
 api/notice/search?q=name
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `name`      | `string` | **Required**. name of what you what to search |

#### POST notice

```http
 api/notice
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `title` | `string` | **Required**. The title of your notice. |
| `event` | `string` | The type of event. |
| `imageUrl` | `string` | The URL of the image associated with the notice. |
| `description` | `string` | **Required**. A detailed description of the notice. |
| `link` | `string` | A link related to the notice. |


#### PUT notice

```http
 api/notice/:id
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `title` | `string` | 	The updated title of the notice. |
| `event` | `string` | The updated type of event for the notice. |
| `imageUrl` | `string` | The updated URL of the image associated with the notice. |
| `description` | `string` |  The updated detailed description of the notice. |
| `link` | `string` | The updated link related to the notice |

#### DELETE notice

```http
 api/notice/:id
```

| Parameter | Type     | Description                                       |
| :-------- | :------- | :------------------------------------------------ |
| `id`      | `string` | **Required**. The unique identifier of the notice to be deleted. |
