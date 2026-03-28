# Supabase learning

## Supabase setup 

### Supabase SSR
Server Side Rendering- all pages loaded on server and sent to client
Next.js
Pages 


### Supabase Client Only SPA
Client loads all data
If using React then have to use Supabase createClient because it is a SPA
SPA created with Vite do client side rendering

Is less secure here because data passes through client

Good for hackathons and small projects
createClient()

works by connecting to suapbase client
import { createClient } from '@supabase/supabase-js'

const supabase = createClient(
  import.meta.env.VITE_SUPABASE_URL,
  import.meta.env.VITE_SUPABASE_ANON_KEY
)

To ensure that users still are authenticated
1. Setup supabase client in react with createclient
2. Sign up/ Login users
- Use supabase auth methods supabase.auth.signInWithPassword()
3. Check if user is logged in
- Use supabase.auth.getsession, 
